# 프로젝트 소개   
* punch 소개   
* 기술소개   
   
# Punch 소개   
펀치는 기존의 출석체크 프로그램의 단점을 보완한 출석체크 플렛폼입니다.    
기존의 출석체크 비밀번호나 QR코드를 이용해 출석체크를 하는 방식은 비밀번호나 QR코드가 유출되서 부정출석이 될 여지가 있었습니다.    
저희 Punch 출석체크는 QR코드를 OTP 형식으로 구현하여 SNS나 영상통화를 통해서 QR코드가 유출되는것을 방지하였습니다.   
또 깔끔하고 편리한 UI를 구축하였습니다.   
   
# Punch 플렛폼   
펀지는 출석체크를 위한 교수용 웹사이트와 학생을 위한 모바일 앱 그리고 수업중 QR코드를 출력하는 GUI 윈도우 프로그램으로 나뉩니다.    
   
# 교수용 웹사이트   
## 로그인 페이지   
<img src="/FrontEnd/자료들/login.gif">   
교수 아이디를 통해서 로그인할 수 있습니다.  

## 수업 페이지   
<img src="/FrontEnd/자료들/ready.png">   
- 왼쪽부터, 사이드바, 수업목록, 선택된수업 으로 공간이 구분되어 있습니다.    
   - 사이드바 : 새로운 수업생성, 설정, 로그아웃 버튼이 있습니다.    
   - 수업목록 : 내가 생성한수업의 목록이 표시됩니다. 클릭하면 선택한수업에 해당수업이 표시됩니다.   
   - 선택된수업 : 수업목록에서 선택한 수업을 표시합니다. 선택된 수업이 없으면 수업을 선택하라는 알림이 표시됩니다.    

## 출석체크 준비   
<img src="/FrontEnd/자료들/qrReady.png">   
   - #1 할일선택 에서 선택된 수업에서 출석체크를 누르면 출석체크를 할 수 있다    
   - #2 출석체크 주차 선택에서 에서 지난 출석체크를 이어서 할것인지 새로운 출석체크를 할것인지 선택할 수 있다.   
   - #3 출석기준 시간에서 지금시간을 기준으로 출석체크를 할것인지 수업시간을 기준으로 출석체크를 할것인지 선택할 수 있다.   
마지막으로 QR생성 버튼을 누르면 출석체크 화면으로 넘어간다    
   
## 출석체크   
<img src="/FrontEnd/자료들/qrmaker.gif">   
출석체크 화면입니다 
- 왼쪽에서 학생들의 목록을 볼수 있으며 특정 학생을 검색할 수 있습니다.
 - 학생을 클릭해서 출결상태를 수동으로 변경할 수 있습니다.
 - 출결기록이 없는경우 학생이 미출석으로 표시되며 부정출석체크가 감지되는경우 (사용하던 핸드폰이 아니라 다른 핸드폰으로 로그인됨) 부정출석 의심이라는 표시가 뜹니다.
 - 해당 학생목록은 실시간으로 연동됩니다. 따라서 학생이 출석체크를 하면 즉시 학생목록에 반영됩니다.
- 오른쪽에서는 출석체크 QR코드가 뜹니다. QR코드는 1초에 한번씩 갱신됩니다. 
 - 아래의 프로그램 아이콘을 클릭해서 윈도우 프로그램이 설치되어 있는경우 윈도우 프로그램을 실행시킵니다.
 
## 출결현황
<img src="/FrontEnd/자료들/list.png">   
학생들의 출석리스트를 보고 수정할 수 있습니다.   
왼쪽에서 주차를 선택하면 오른쪽에서서 해당 주차의 출결리스트를 확인할 수 있습니다.   
출결리스트 아래의 학생들은 편집할수 있습니다.   

## 수업생성
<img src="/FrontEnd/자료들/make.gif">   
사이드바의 수업 생성버튼을 통해서 수업을 생성할 수 있습니다. 
수업을 생성할때 필요한것은 2가지 입니다. 수업이름과 수업시간입니다. 수업시간은 분할수업을 고려하여 여러개 생성할 수도 있습니다. 
또 수업의 색상과 지각&결석인정 시간을 지정할 수도 있습니다. 

## 수업 바로가기
<img src="/FrontEnd/자료들/go.gif">   
최근에 QR코드를 생성한 수업이 있으면 하단에 진행중인 수업 바로가기 버튼이 나옵니다.   
바로가기를 클릭하면 수업으로 이동합니다.

## 수업삭제
선택된수업에서 설정 버튼을 눌러서 수업을 삭제할 수 있습니다.
수업을 삭제하기위해서는 비밀번호를 다시 입력해야합니다.

# 학생용 모바일앱   
## 로그인 화면
<img src="/FrontEnd/자료들/mlogin.png">   
학생 아이디를 사용해서 로그인 할 수 있습니다.
## 수업목록
<img src="/FrontEnd/자료들/mmain.png"> 
참여중인 수업 목록을 볼 수 있습니다. 수업을 누르면 해당 수업의 출결 현황으로 넘어갑니다.
## 출결현황
<img src="/FrontEnd/자료들/mlist.png">   
내 출석 현황을 볼 수 있습니다.
## 출석체크
<img src="/FrontEnd/자료들/mQR.png">
카메라를 통해서 QR코드를 찍어서 출석체크를 할 수 있습니다.
