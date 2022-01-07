# PDF-Editor
> ## 👉 Introduction
> > PDF 편집(병합, 분할 등)을 위해서는 ezPDF 등 편집 프로그램을 구매해야 되거나 별도 인터넷 웹 사이트에 접속해야 하는데, PDF 편집을 몇 번 하지 않는데도 비용을 부담하는 것은 꺼려지고 웹 사이트에 접속해서 편집하는 경우 로딩시간, 광고 노출 등 번거로움이 발생하여 파이썬을 통해 자체 프로그램을 개발하여 문제를 해결하고자 했습니다.

<br/>
<hr/>
<br/>

> ## 👏 Overview
> > ### Functions
> > > +  PDF 분할 및 병합 📑
> > > +  마우스 드래그 앤 드롭 🖱
> > > +  PDF 병합 순서 변경 및 선택 삭제 ✂
> > ### Tech
> > > #### Programming Language / Library
> > > + Python, tkinter, PyPDF2, TkinterDnD2  
> > > #### IDE
> > > + Visual Studio Code
> > > #### Production Period
> > > + 2021년 4월 1일 ~ 2021년 4월 15일(기능 구현)
> > > + 2021년 5월 4일(기능 개선)
> > > + 2021년 7월 9일(기능 개선)
> > > #### Information
> > > + 해당 프로그램으로 별도 수익을 창출하지 않습니다.
> > > + 지인들이 실제 현업에서 사용 중이며 만족도가 높습니다. 👍

<br/>
<hr/>
<br/>

> ## 🛠️ Details
> > ### ① 프로그램 전체 프레임 구성
> > > + 파일 프레임
> > >   +  PDF 파일 추가(디렉토리 조회)
> > >   +  리스트 프레임 상 PDF 파일 순서 변경
> > >   +  리스트 프레임 상 PDF 파일 선택 삭제
> > > + 리스트 프레임
> > >   + 리스트 박스(마우스 드래그 앤 드롭)
> > >   + 세로 스크롤바
> > > + 저장 경로 프레임
> > >   + 저장경로 찾기(디렉토리 조회)
> > >   + 저장경로 입력란 및 가로 스크롤바
> > > + 실행 프레임
> > >   + PDF 파일 분할 및 병합 실행 버튼
> > >   
> > > ![캡처](https://user-images.githubusercontent.com/82401504/146517919-2ca6d9b6-cc0d-46a9-8e0a-64386694e545.PNG)
> >   
> > ### ② PDF 병합 순서 변경 및 선택 삭제
> > > 여러 개의 PDF 파일을 병합 시 '↑ ', '↓' 버튼을 클릭하여 병합되는 순서를 변경할 수 있습니다
> > > ![image](https://user-images.githubusercontent.com/82401504/145345668-9f567d1f-40da-4ceb-b38f-a5bf65dc247e.png)
> > > #### Features
> > > + 순서 변경 시 해당 파일이 리스트를 벗어나지 않도록 index 제한 설정
> > > + pdf 파일 삭제 시 reversed()를 통해 역순으로 정렬 후 for문을 통해 삭제
> > >   + index 0 ~7의 pdf 파일이 있다고 했을 때, 0을 먼저 삭제 하면 뒤에 있는 pdf 파일이 앞으로 오기 때문에 나중에 7이 삭제되지 않기 때문
> >
> > ### ③ 마우스 드래그 앤 드롭
> > > PDF 파일이 깊은(복잡한) 디렉토리에 존재하는 경우 디렉토리를 타고 PDF 파일을 등록하기 번거로우므로 파일을 끌어다가 프로그램에 직접 등록시킬 수 있습니다.
> > > 
> > > ![image](https://user-images.githubusercontent.com/82401504/146517646-757f15f0-7e89-4410-bfd1-dcea60f3f1b2.png)
> > > #### Features
> > > + TkinterDnD2 라이브러리의 drag_source_register, dnd_bind 등의 메서드와 widget 속성 활용
> >
> > ### ④ PDF 분할 및 병합
> > > 여러 페이지의 PDF를 분할할 수 있고 여러 개의 PDF 파일을 병합하여 새로운 PDF 파일을 생성할 수 있습니다.
> > > 
> > > ![image](https://user-images.githubusercontent.com/82401504/145346415-332fc569-7c3e-49e5-ad99-111a18c6e52d.png)
> > > #### Features
> > > + PyPDF2 라이브러리의 PdfFileWriter 및 PdfFileReader 객체를 통한 pdf 파일 분할
> > > + PyPDF2 라이브러리의 PdfFileMerger 객체를 통한 pdf 파일 병합

<br/>
<hr/>
<br/>

> ## 🎞 Retrospection
> > 개발자가 되기로 결심한 후 제가 처음 프로그래밍 언어로 배운 것은 파이썬이었습니다. 유튜브 “나도 코딩” 채널을 통해 파이썬을 학습했었는데, 파이썬 기초 문법을 학습하고 파이썬 라이브러리를 통해 게임, 이미지 병합 프로그램, 웹 스크래핑, 업무자동화(RPA) 프로그램을 만들어 보는 과정(클론 코딩)이었습니다.
> > 
> > 해당 과정을 통해 배운 내용을 토대로 개인적으로 PDF 편집 프로그램을 개발해 보고 싶었습니다. 저의 전 직장에서는 PDF 편집을 위해서는 별도 프로그램(법인용)을 구매해야 하거나 별도 웹 사이트에 접속해야하는 불편함이 있었습니다. 이러한 문제를 해결해보고자 사용자 입장에서 어떻게 PDF 편집을 편리하게 할 수 있을지 고민해보며 위 과정에서 다루지 않았던 PDF 병합·분할이나 마우스 드래그 앤 드롭 라이브러리 사용법을 찾아가면서 PDF 편집 프로그램을 개발해 보았습니다. 이후 개발한 프로그램을 지인들에게 배포해본 결과 모두들 현업에서 사용 만족도가 높았으며 또한 어떤 점이 불편했는지(PDF 파일 등록이 불편하다, 저장경로 확인이 불편하다 등) 피드백을 받아 기능을 개선시킬 수도 있었습니다.
> > 
> > 이를 통해 개발 공부는 무엇보다 실제로 서비스를 개발해보고 이를 사용자들에게 배포하고 운영해보는 것이 가장 효과적인 학습 방법이라는 것을 느낄 수 있었습니다. 또한 프로그래밍을 통해 자신의 아이디어가 소프트웨어로 실제화되어 구현될 때 느끼는 희열감과 어떤 문제에 대해 고뇌하는 끝에 해결될 때 얻는 성취감 그리고 사용자가 편리함을 느낄 때 보람감을 느낄 수 있었고 이러한 것들이 개발자가 프로그래밍을 하는 이유이지 않을까라고 생각해볼 수 있었습니다.

