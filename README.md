# WEBPROJECT_ARCADE_GAMEPAGE
This repository includes webProgramming project- [Arcade Gamepage(고전게임을 즐길 수 있는 사이트)]


### 팀프로젝트 소개 영상(발표 영상)
[https://youtu.be/5S9DC8npByQ](https://youtu.be/5S9DC8npByQ)


### 프로젝트 결과 보고서

웹프로그래밍 프로젝트 보고서
- 고전게임 사이트 만들기 - 

5팀 : 고유진(2016116742) 
김이랑(2017117034)
	최민호(2016111316)
이은찬(2015110553)

프로젝트 제목 : 고전게임 사이트 만들기

프로젝트 주제 
: 독창적인 요소가 들어간 고전 게임 사이트 제작익숙하고 잘 알려진 고전게임인 ‘틀린그림찾기’, ‘숨은그림찾기’, ‘같은그림찾기’, ‘노노그램’에 독창적인 요소를 추가해 웹프로그램으로 직접 구현해보았다. (추가, 수정)

주제 선택 동기
그간 배운 내용인 HTML, CSS, JS, JSP를 사용하되, 독창적으로 구현해 볼 수 있는 웹 사이트를 선정하기 위해 의논한 후, 고전 게임 사이트 제작이라는 주제를 선정하게 되었다.
 팀을 구성한 후 개발해보고 싶었던 주제를 의논해보았는데, 신기하게도 팀원 모두가 게임 제작과 관련된 프로젝트를 진행하고 싶어하였다. 따라서, 팀원 각각 고전게임 하나씩 개발을 맡아 ‘틀린그림찾기’, ‘숨은그림찾기’, ‘같은그림찾기’, ‘노노그램’을 구현해보기를 결정하고, 독창적인 요소를 추가하여 웹 프로그램을 개발하는 프로젝트를 진행하였다.

팀원 간 역할 분배
팀원 4명이 각자 게임 1개를 맡아 Javascript로 고전게임 사이트의 핵심인 게임 로직을 구현한 뒤, 홈화면, 데이터베이스, 로그인, 메뉴로 파트를 나눠 웹사이트를 완성하였다. 맡은 부분을 구현 한 후 각자 개발한 파트의 보고서 및 발표 자료를 제작하고 보고서 작성, 발표자료 작성, 동영상 자료 제작 및 소스 코드 취합을 다음과 같이 나누어 진행하였다. 

고유진 : 노노그램, menu.jsp, 발표 자료 제작
최민호 : 숨은그림찾기, 로그인, 동영상 자료 제작
김이랑 : 틀린그림찾기, 데이터베이스, 보고서 작성
이은찬 : 같은그림찾기, 웹페이지 홈화면, 소스 코드 취합 

제작기간 및 , 일정
제작 기간 및 일정은 다음과 같다.


 



소스코드 주소 
추가해주세영~~!

파일 구조도, 설명

웹사이트 설명(홈화면, 데이터베이스, 로그인, 메뉴 / 게임별 설명)
1) 기본 구조 설명
홈화면, 데이터베이스, 로그인, 메뉴


홈화면
 
홈화면은 사용자가 접속했을 때 가장 먼저 접하게 되는 화면이다. 간결한 디자인으로 구현하여 사용자가 원하는 메뉴를 클릭할 수 있도록 도움을 준다. 화면 상단 메뉴바를 통해 원하는 게임을 선택할 수 있다.  메뉴바에 마우스를 올리면 하위 테이블을 보여준다. 화면 ‘body’ 부분에는 소개 글과 함께 고전게임 테마에 맞는 이미지를 첨부하였다. 




메뉴
 
‘Home’을 클릭하면 홈화면으로 이동하고, 게임 이름을 클릭하면 클릭한 게임 페이지로 이동한다. 페이지 모듈화를 위해 따로 jsp파일로 제작되었으며, 모든 게임 코드의 가장 위에 파일을 삽입하여 게임 페이지 상단에 위치한다. 



로그인
로그인 기능은 사용자 데이터베이스와 세션으로 구현하여 서버와의 지속된 연결과 사용자 정보 관리를 고려하였다. 아래의 우측 그림은 회원가입을 위한 창으로, 처음 사용하는 사용자는 아이디와 비밀번호 외의 개인정보들을 입력해야 한다. 아이디와 비밀번호의 경우, 아이디 중복 검사와 유효성 검증을 통해 사용자 정보 관리의 편의와 일관성을 얻을 수 있도록 하였다. 유효성 검증에 통과된 경우 회원가입이 진행되며 해당 정보들은 서버의 데이터베이스 gameUserDB에 저장된다. 이후, 좌측 그림의 로그인 창을 통해 사용자는 로그인을 할 수 있다. 로그인의 검증을 위해 gameUserDB에서 입력된 아이디와 비밀번호와 일치되는 사용자 정보를 찾아 사용자를 확인한다. 이후, 로그아웃을 할 경우 서버에 저장된 사용자의 세션을 제거하여 사용자와 연결을 중단하도록 하였다.
      

데이터 베이스
데이터베이스로는 MySQL을 사용하였다. ‘DBManager’ 라는 클래스를 따로 생성하여 데이터베이스 커넥션을 관리하도록 했다. 해당 클래스에서는 JDBC_DRIVER의 이름과 DB_URL, 데이터베이스의 유저이름과 비밀번호를 관리한다. 
다른 클래스에서 ‘DBManager’ 객체를 생성하면 자동으로 데이터베이스와 커넥션이 맺어지고, 원하는 SQL 문장을 만들어서 ‘DBManager.select(String sql)’이나 ‘DBManager.update(String sql)’ 메소드로 넘겨줄 수 있다. 메소드가 실행되면 DBManager의 ResultSet 객체에 결과가 저장되고, 해당 객체를 이용해 결과를 클라이언트에게 보내줄 수 있다. 
모든 SQL 질의가 끝난 후에는 반드시 ‘DBManager.close()’ 메소드를 호출하여 커넥션을 종료하도록 해야한다.
이렇게 데이터베이스를 관리하는 클래스를 따로 만들어줌으로써 다른 클래스에서 재사용 하기에 용이하도록 구현하였다. 내꺼적기

2. 게임별 설명 – 룰, 스크린샷
1. 같은 그림 찾기 
고전적인 로직인 [같은 그림 찾기] 기능을 웹 프로그램으로 직접 구현해보았다.   

룰은 아래와 같다.
1. 마우스를 클릭해서 같은 이미지를 두개씩 짝을 지어서 맞추면 된다.
2. 라운드는 1라운드(4x4), 2라운드(5x5), 3라운드(6x6)를 지원한다.
3. 점수는 맞추면 10점 틀리면 -5점에 연속 정답/오답에 대한 추가 점수가 적용된다.
4. -100점 이하가 되면 패배하게 되며 모든 그림이 오픈되며 게임이 끝난다.


그림 클릭 처리와 정답/오답 판별 로직, 점수 업데이트 등에서 JavaScript를 이용했으며, 그림은 라운드(이미지 수)에 따라 동적인 for-루프로 받아온다. Javascript에서 HTML태그 특정 id 위치의 텍스트를 변동할 수 있는 getElementById와 innerHTML 메소드를 많이 사용하였으며 더 나은 기능 구현을 위해 JQuary($) 를 일부 사용하였다




(1) 틀린 그림 찾기 
2. 틀린 그림 찾기
 틀린 그림 찾기는 두 개의 이미지 중 틀린 부분을 찾는 게임이다. 난이도에 따라 데이터베이스에 저장된 이미지와 각 이미지에 대한 정답 좌표를 서버에 요청하여 받아서 JSP 상에 보여준다. 각 난이도마다 라운드는 총 3개이고, 라운드 마다 이미지는 서로 중복되지 않도록 서버에서 로직을 구현했다. 각 라운드에 대한 이미지 요청은 주소에 라운드번호와 난이도를 표시하여 GET요청을 하도록 구현했다.

각 이미지는 데이터베이스에 (이미지 번호, 난이도)로 저장되어 있다.
각 이미지에 대한 정답은 (이미지 번호, X좌표, Y좌표, 사이즈)로 저장되어 있다.

	
틀린 그림 찾기 게임 시작 화면이다. ‘Easy’, ‘Normal’, ‘Hard’ 3가지 난이도를 선택한 후, 하단의 시작 버튼으로 게임을 시작할 수 있다.
총 3라운드로 구성되어 있으며, 라운드 간에 이미지는 중복되지 않으며 제한 시간은 모두 60초로 설정되어 있다. 
정답인 곳을 클릭하면 빨간 원이 그려지며, 틀린 곳을 클릭할 시에는 시간이 5초 차감된다. 제한 시간 내 모든 답을 맞히면 다음 라운드로 진행되지만, 제한 시간 내 모두 찾지 못하면 게임 시작 화면으로 되돌아간다. 

	

‘Normal’ 난이도 선택 후, 게임이 시작된 화면이다. 좌측에는 사진 2장과 남은 시간이 표시된다. 우측에는 현재 라운드와 난이도, 현재 찾은 틀린 그림 개수와 전체 틀린 그림 개수가 나타난다.

(2) 
3. 숨숨은 그림 찾기
숨은 그림 찾기는 하나의 큰 그림 안에 부적절하지만, 형태의 유사성을 가진 작은 그림들을 숨겨두고 참여자는 숨겨진 그림을 찾는 게임이다. 본 게임에선 Java상에 저장된 숨은 그림과 타겟 이미지, 타겟들의 위치 정보들을 불러와 Javascript를 통해 구현하였다. 게임은 4개의 스테이지가 있으며, 설정 모드를 통해 타겟의 개수와 시간 제한을 동적으로 수정할 수 있게 하였다.

	게임의 진행 화면, 하측에 있는 다섯 개의 이미지가 위의 그림에서 찾아야 하는 숨은 타겟이다. 숨은 그림에서 타겟의 직사각형으로 표현된 위치 안에 마우스의 입력을 할 경우, 마우스의 위치 정보를 사용하여 타겟 주변에 빨간색의 발견 표시를 구현하였다. 
잔여 시간은 좌측 상단에 파란 사각형과 빨간 사각형을 통해 구현하였다. 파란 사각형은 시간이 지남에 따라 폭이 감소하게 되고 파란 사각형이 없어질 경우 제한 시간이 끝나 게임에 실패하게 된다. 우측 상단에는 전체 타겟 중에서 발견한 타겟과 해당 스테이지를 표현하였다.
	만일, 스테이지에서 제한 시간 내에 모든 타겟을 찾지 못했을 경우 좌측과 같은 화면을 확인할 수 있다. 게임에서 실패했을 경우, 해당 스테이지를 다시 반복하는 ‘다시 하기’와 정답을 확인할 수 있는 ‘정답 보기’, 설정 모드를 통해 난이도를 조절할 수 있는 ‘설정’ 버튼을 사용할 수 있다.
	좌측 이미지는 설정 모드에 들어가면 볼 수 있다. 설정 창에서는 제한 시간과 타겟의 개수를 조절하여 난이도를 조절할 수 있다. 제한 시간은 30초에서 180초까지, 타겟은 5개에서 9개까지 설정 가능하다. 초기값으로는 120초와 5개로 지정하였다. 해당 모드는 게임의 시작과 게임에 실패했을 때 사용할 수 있다. 
좌측 하단에 위치한 작은 이미지는 게임에서 실패하였을 때, ‘정답 보기’를 통해 정답을 확인할 수 있는 이미지이다.


(3) 같은 그림 찾기 
고전적인 로직인 [같은 그림 찾기] 기능을 웹 프로그램으로 직접 구현해보았다.   

룰은 아래와 같다.
마우스를 클릭해서 같은 이미지를 두개씩 짝을 지어서 맞추면 된다.
라운드는 1라운드(4x4), 2라운드(5x5), 3라운드(6x6)를 지원한다.
점수는 맞추면 10점 틀리면 -5점에 연속 정답/오답에 대한 추가 점수가 적용된다.
-100점 이하가 되면 패배하게 되며 모든 그림이 오픈되며 게임이 끝난다.

그림 클릭 처리와 정답/오답 판별 로직, 점수 업데이트 등에서 JavaScript를 이용했으며, 그림은 라운드(이미지 수)에 따라 동적인 for-루프로 받아온다. Javascript에서 HTML태그 특정 id 위치의 텍스트를 변동할 수 있는 getElementById와 innerHTML 메소드를 많이 사용하였으며 더 나은 기능 구현을 위해 JQuary($) 를 일부 사용하였다.

	기본화면 5x5의 기본 화면이다. 메인 보드는 게임명과 게임 시작 버튼, 점수 테이블로 구성된다. 아랫 줄에 상태창은 게임 진행을 위한 도움말과 게임 상황에 대한 텍스트를 출력한다. 가장 아래에 게임 화면이 있으며 기본화면의 경우 그림이 아직 닫혀 있다.	
	
게임 시작 버튼을 누르면 상태창은 5초의 카운팅을 시작하며 5초가 지나면 모든 그림을 뒤집는다. 그러므로 게임 이용자는 그림이 열리는 5초동안 그림을 유심히 보는 것이 유리하다.

.	
	5초가 지나면 모든 그림을 뒤집는다. 5x5의 경우 그림이 홀수이므로 게임 진행을 위해 가운데 라이언 그림은 자동으로 열리게 되며 라이언 그림은 2장이 아닌 1장이다.

게임 시작을 알리는 상태창 알림과 함께 게임시작 버튼이 다시하기 버튼으로 바뀐다.	


4. 노노그램
노노그램은 바둑판 모양의 판에 숫자 지시에 따라 칸을 클릭하면 그림이 나오는 게임이며, 난이도에 따라 1단계, 2단계로 구분하였다. 이번 프로젝트에서는 Javascript, Jquery에 초점을 두어 구현하였다. 

	홈화면, 메뉴에서 노노그램을 클릭했을 때 표시되는 노노그램의 시작화면이다. 
각 단계별 제한 시간은 3분, 5분이며, 상단의 ‘남은 시간’에서 남은 시간을 초 단위로 확인할 수 있다. 또한 각 단계 별로 3번의 기회가 주어진다. 이는 정답이 아닌 칸을 클릭했을 때 한 개씩 차감되며 ‘남은 시간’ 옆의 하트 모양으로 남은 기회를 확인할 수 있다. 
[START] 버튼 클릭과 동시에 노노그램 게임 화면이 나타나고 타이머가 동작해서 남은 시간을 확인할 수 있다. 


게임의 성공은 제한 시간 내에 3번의 기회 내에서 모든 정답칸을 클릭했을 때이며, 이 경우에만 소요시간, 등수를 확인할 수 있다. 등수는 소요시간 순으로 정해진다. 등수에서 사용하는 다른 소요시간은 미리 다른 사용자가 게임을 수행한 후 걸린 시간을 코드 안에 배열로 넣었다. 
제한 시간 안에 노노그램의 모든 정답칸을 클릭하지 못하였거나, 3번의 기회가 모두 차감될 경우에는 실패이며, 소요시간과 등수 확인이 불가능하다. 	
틀린 그림 찾기 게임 시작 화면이다. ‘Easy’, ‘Normal’, ‘Hard’ 3가지 난이도를 선택한 후, 하단의 시작 버튼으로 게임을 시작할 수 있다.
총 3라운드로 구성되어 있으며, 라운드 간에 이미지는 중복되지 않으며 제한 시간은 모두 60초로 설정되어 있다. 
정답인 곳을 클릭하면 빨간 원이 그려지며, 틀린 곳을 클릭할 시에는 시간이 5초 차감된다. 제한 시간 내 모든 답을 맞히면 다음 라운드로 진행되지만, 제한 시간 내 모두 찾지 못하면 게임 시작 화면으로 되돌아간다. 

	

‘Normal’ 난이도 선택 후, 게임이 시작된 화면이다. 좌측에는 사진 2장과 남은 시간이 표시된다. 우측에는 현재 라운드와 난이도, 현재 찾은 틀린 그림 개수와 전체 틀린 그림 개수가 나타난다.
	게임의 진행 화면, 하측에 있는 다섯 개의 이미지가 위의 그림에서 찾아야 하는 숨은 타겟이다. 숨은 그림에서 타겟의 직사각형으로 표현된 위치 안에 마우스의 입력을 할 경우, 마우스의 위치 정보를 사용하여 타겟 주변에 빨간색의 발견 표시를 구현하였다. 
잔여 시간은 좌측 상단에 파란 사각형과 빨간 사각형을 통해 구현하였다. 파란 사각형은 시간이 지남에 따라 폭이 감소하게 되고 파란 사각형이 없어질 경우 제한 시간이 끝나 게임에 실패하게 된다. 우측 상단에는 전체 타겟 중에서 발견한 타겟과 해당 스테이지를 표현하였다.
	만일, 스테이지에서 제한 시간 내에 모든 타겟을 찾지 못했을 경우 좌측과 같은 화면을 확인할 수 있다. 게임에서 실패했을 경우, 해당 스테이지를 다시 반복하는 ‘다시 하기’와 정답을 확인할 수 있는 ‘정답 보기’, 설정 모드를 통해 난이도를 조절할 수 있는 ‘설정’ 버튼을 사용할 수 있다.
	좌측 이미지는 설정 모드에 들어가면 볼 수 있다. 설정 창에서는 제한 시간과 타겟의 개수를 조절하여 난이도를 조절할 수 있다. 제한 시간은 30초에서 180초까지, 타겟은 5개에서 9개까지 설정 가능하다. 초기값으로는 120초와 5개로 지정하였다. 해당 모드는 게임의 시작과 게임에 실패했을 때 사용할 수 있다. 
좌측 하단에 위치한 작은 이미지는 게임에서 실패하였을 때, ‘정답 보기’를 통해 정답을 확인할 수 있는 이미지이다.
	기본화면 5x5의 기본 화면이다. 메인 보드는 게임명과 게임 시작 버튼, 점수 테이블로 구성된다. 아랫 줄에 상태창은 게임 진행을 위한 도움말과 게임 상황에 대한 텍스트를 출력한다. 가장 아래에 게임 화면이 있으며 기본화면의 경우 그림이 아직 닫혀 있다.	
	
게임 시작 버튼을 누르면 상태창은 5초의 카운팅을 시작하며 5초가 지나면 모든 그림을 뒤집는다. 그러므로 게임 이용자는 그림이 열리는 5초동안 그림을 유심히 보는 것이 유리하다.

.	
	5초가 지나면 모든 그림을 뒤집는다. 5x5의 경우 그림이 홀수이므로 게임 진행을 위해 가운데 라이언 그림은 자동으로 열리게 되며 라이언 그림은 2장이 아닌 1장이다.

게임 시작을 알리는 상태창 알림과 함께 게임시작 버튼이 다시하기 버튼으로 바뀐다.	
	같은 그림을 찾으면 상태창의 알림이 Great과 함께 점수 변화를 알려준다. 그 후 그림은 닫히지 않고 유지되며 점수창의 점수가 업데이트 된다.	
	마지막 쌍을 맞추게 되어 모든 같은 그림쌍을 찾으면 축하 ALERT와 함께 게임은 끝난다.

[ Clear!! Your Score : {점수} !! 짝짝짝짝 ]	
	홈화면, 메뉴에서 노노그램을 클릭했을 때 표시되는 노노그램의 시작화면이다. 
각 단계별 제한 시간은 3분, 5분이며, 상단의 ‘남은 시간’에서 남은 시간을 초 단위로 확인할 수 있다. 또한 각 단계 별로 3번의 기회가 주어진다. 이는 정답이 아닌 칸을 클릭했을 때 한 개씩 차감되며 ‘남은 시간’ 옆의 하트 모양으로 남은 기회를 확인할 수 있다. 
[START] 버튼 클릭과 동시에 노노그램 게임 화면이 나타나고 타이머가 동작해서 남은 시간을 확인할 수 있다. 
	게임이 시작된 후 화면이다. 
표의 1행, 1열에 나타나 있는 숫자는 각 행, 열에서 클릭해야하는 칸의 숫자이다. 이 숫자 지시를 따라 정답칸을 찾아 클릭한다. 정답칸을 클릭했을 때에는 색깔이 표시되고 정답이 아닌 칸을 클릭했을 경우, X가 표시되며 한 번의 기회가 차감된다. 
우측 상단의 물음표 그림에 마우스를 올리면 모든 정답칸을 클릭했을 때 완성되는 그림을 힌트로 보여준다. 
			게임이 끝난 후의 화면이다. 
첫번째 사진은 성공했을 때, 두번째 사진은 시간초과로 실패했을 때, 세번째 사진은 3번의 기회가 모두 차감되었을 때 나타나는 화면이다. 성공했을 때 [2단계] 버튼을 클릭하면 노노그램 2단계로 이동하고 실패했을 때 [다시 시도] 버튼을 클릭하면 노노그램 1단계를 다시 시도할 수 있다. 