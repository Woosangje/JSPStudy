# JSPStudy

0130
javax는 톰켓9버전

edu > new > Servlet > java packge : core

생성후 Servers > 톰켓 들어가서 해당 DB만 선택 > finish

톰캣 > clean
실제pc의 크롬에서  http://192.168.111.101:8000/edu/FirstServlet
404페이지가 안뜨면 정상

FirstServlet에 입력하고
servers 중지후 다시 start

초기화는 한번만

404에러가뜨면 무조건 주소가 잘못된것, 파일명과 주소명이 달라야 해킹하기 어려움<br>

서블릿메소드는 통로라고 생각해야한다.<br>
요청, 응답<br>

???? 발생하면 유니코드 잘못입력했는지 확인<br>

★    <welcome-file>index.html</welcome-file><br>
비어있는 목록을 해커가 만들수 있으니 하나만 사용할것<br>

Application Server = 톰켓 was<br>
★ 400, 500번 에러 알기 http상태코드<br>
https://hongong.hanbit.co.kr/http-%EC%83%81%ED%83%9C-%EC%BD%94%EB%93%9C-%ED%91%9C-1xx-5xx-%EC%A0%84%EC%B2%B4-%EC%9A%94%EC%95%BD-%EC%A0%95%EB%A6%AC/<br>

http://192.168.111.101:8000/edu/new2<br>
f12 > Network > f5 >header >  status Code : 200인지 확인<br>

url로 들어오는 것을 파라메터라 부른다.<br>
get방식은 주소뒤에 ?k=v 가 붙는다.<br>

검색한 언어가 컴퓨터에 저장되어있음 쿠키<br>
★4.4 요청 재지정(중요) 한자웹서블릿58p<br>
★ 347p RequestDispatchar rd = request.getRequestDispatcher 외우기<br>

forwardServlet사용시 output.html 파일 만들어야한다<br>
포워드 방식 외우기<br>
스프링부트 중요<br>
352 74p 서블릿은 한번 읽고 말기<br>
jsp가 가장 어려움<br>

(오라클, 자바) > jdbc > 서블릿 > 톰켓 <  thml > jsp<br>
was = 톰켓<br>

★★★★★ JSP<br>
이클립스 > new > new dynamic web project :이름은 MustHaveJSP<br>
Generate 토글 on하기<br>

WEB-INF > web.xml > jsp에서 쓸만한 코드 입력 필요없는건 지워도된다.<br>
확장자가 jsp<br>

탭의 window > jsp file이 utf-8인지 확인<br>
MustHaveJSP오른쪽클릭  > Perference  utf-8인지 확인<br>

webapp우클릭 jspfile생성<br>
<%!   %><br>
<%= str1  %><br>

톰켓 > clean > add and remove 추가<br>

500에러는 서버에러 코드가 노출되기 때문에 try/catch로 에외처리한다.<br>

지시어 <%@ 에다가 isErrorPage="true" 선언해야 한다.<br>

★★★trimDirectiveWhitespaces 속성<br>
모바일에서 html 공백있을시 에러발생할수 있어서 선언<br>
★★★ inclue 지시어  자주사용(jsp 파일안의 jsp 파일 header나 footer같은거)<br>

표현식<br>
