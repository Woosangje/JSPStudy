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

0131<br>
집에서 jsp공부하기<br>
HelloJSP<br>
라이프사이클 , 2.톰켓사용(jdbc관장) 3.cookie(유효기간) 4. section(로그인-로그아웃까지) 5.reDirect, forward<br>
jdbc는 설치가 절반 부록B 보면서 설치하기<br>


Mime Type<br>

프로그래밍 3번 많이치기, 외워서 치기, 응용해서 치기<br>

※MustHaveJSP<br>
02ImplicitObject<br>
★구글 url 디코드 검색<br>

★ post방식으로 submit 하면 한글 깨짐 request.setCharacterEncoding("UTF-8");<br>
★ Enumeration은  import걸어야 한다.<br>
★ request.getParameter("eng") 자주사용<br>
★ request.getRequestDispatcher("ResponseMain.jsp?loginErr=1").forward(request, response);<br>
null이아니게 1로 변경<br>

web.xml edu에 대한<br>
web.xml 의 필요없는 welcome-file 지우기<br>

driver, url, id, password를 application에다가 저장<br>
★ web.xml 에서 location선언하고 Exception.jsp 만들어야 한다.<br>
<error-code>405</error-code>,  response.getStatus(); , string = 404;<br>
★★★ 브라우저 <br>
session(로그인 정보 유지) > request(아이디, 로그인 정보 주고받음) > page(처리)<br>
★★★ 자바빈즈(JavaBeans)<br>
java파일 new > other > class파일 common 생성<br>
★pageContext : 페이지영역<br>
★pageContext.setAttribute는 오브젝트(Intger)같이 선언해야한다.<br>

PageInclude.jsp<br>
★ include.jsp의 html은 싹지워도 상관없다.<br>
★ import거는거 잊지 않기 <%@ page import="common.Person" %><br>

Main.jsp의 하단에 	<%@ include file="PageInclude.jsp" %>를 선언하면 메소드처럼 호출할수 있다.<br>
request.get~는 오류 안뜨고 null처리된다.<br>

RequestForward.jsp<br>
세션은 서버 쿠키는 내가<br>
크롬에서 f12 application에서 쿠키삭제해볼수 있음 삭제하면 500에러뜬다<br>

ApplicationMain.js<br>
페이지는 잘안쓰고 장바구니에서 쓰임<br>
Request와 session을 자주 사용<br>


※ 0201
● 04cookie
쿠키는 처음에는 못사용한다 최소 새로고침해야 결과가 나온다.<br/>
쿠키 응답시간은 톰켓에서 막아놈<br/>

크롬 옵션 > 쿠키 데이터 삭제 > CookieMain.js에서 쿠키 삭제됐는지 확인<br/>
★ 쿠키는 팝업 공지시 하루 열지 않기를 원할때 사용<br/>
● PopupMain_01.js<br/>
jquery cdn 주소 붙여넣기<br/>
쿠키를 추가하여 hide 반영구로 적용시키기<br/>
checked 는체크가 되어있다는 뜻<br/>
● url을 위한 PopupCookie.jsp<br/>

★★★ cookie 저장이 안될경우 jquery jdn 을 3.5.1 minified로 선언해야 한다.<br/>
ajax는 관심을 가져야 한다.<br/>
Java Resources에서 java파일 생성가능<br/>

● JSFunction.java, CookieManager.java<br/>
● IdSaveMain , IdSaveProcess.jsp<br/>
쿠키 관련 파일은 그대로 사용하면 된다.	import="utils.CookieManager"<br/>
request.getParameter방식으로 받는다.<br/>

★★★★★★ JDBC<br/>
system.sql > JDBC할때 오라클 CONNECT할것 > common 패키지에 MustHave.sql만들것<br/>
MustHave.sql 파일 생성<br/>
create빌드하고<br/>
Oracle 을 musthave만들고 계정도 musthave, 1234로 일치시킴<br/>
한글 쓰려면 n 붙여야함 nvarchar2(30)<br/>

MustHaveJSP우클릭 > BuildPath > Modulepath > objdbc6추가<br/>
★ 톰켓 경로의 lib에 objdbc6파일 추가<br/>
★ D:\workspace\MustHaveJSP\src\main\webapp\WEB-INF\lib 에다 objdbc6파일 추가<br/>
● JDBConnect.java , 05JDBC > ConnectionTest.jsp<br/>
web.xml로 이동 context-param 값 4개 추가<br/>
