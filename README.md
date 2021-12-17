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
> > > + 전 직장 동료와 지인들이 실제 현업에서 사용 중이며 만족도가 높습니다. 👍

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
> > > ![image](https://user-images.githubusercontent.com/82401504/146517780-7f3ecab6-630e-4744-9585-9bcb1d3f6efb.png)
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




