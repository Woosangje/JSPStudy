# JSPStudy
오류 <br>
★ DTO에 String,int DAO와 일치하는지 확인 <br>
★ rs.getInt() + "\t")인지 확인 getInt(중괄호안에 +"\t"있으면 안됨) <br>
★ updateDAO실행하려면 해당 메소드에<br>
con = DriverManager.getConnection("jdbc:oracle:thin:@sorune.asuscomm.com:15210:xe", "subway", "subway");<br>
재선언해줘야 pstmt is null 오류 안생긴다.		<br>	
★ 톰켓 탭에서 삭제하고 다시 생성하면 port 8010이었던게 - 로 초기화된다.<br>


0130<br>
javax는 톰켓9버전<br>

edu > new > Servlet > java packge : core<br>

생성후 Servers > 톰켓 들어가서 해당 DB만 선택 > finish<br>

톰캣 > clean<br>
실제pc의 크롬에서  http://192.168.111.101:8000/edu/FirstServlet<br>
404페이지가 안뜨면 정상<br>

FirstServlet에 입력하고<br>
servers 중지후 다시 start<br>

초기화는 한번만<br>

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

※ 0202
sql파일 만들어서 가지고 있으면 편함
new를 20개정도 해놓는걸 커넥션 풀
수영장에 튜브를 만들어 놓는다.
이클립스 server > tomcat < server.xml > 20행 61행 포트번호
35행 오타있으면안됨 <GlobalNamingResources> 그대로 복붙하기
\\304-00\수업자료\5. jsp\DBConnPool > server.text를 이용한마
type = "javax.sql.DataSource"   javax는 톰켓버전9
30행 <GlobalNamingResources> 안에다  sever.text 붙이기
DB 바뀌면 name="dbcp_myoracle" 도 수정해야 한다
context.xml에 context.text내용 붙여넣기
● common > DBConnPool.java
CallableStatement는 알필요 없음
● ExeUpdate.jsp
ExeUpdate.jsp는 아이디가 중복되는 한번만 실행하기
웹으로 실행해보고 DB실행하고 sql에서 member실행해서 생성됐는지 확인하기
● ExeQuery.jsp
97p

★★★xml없을 경우 project 파일 생성할대 generator ~xml 토글 체크안해서 그렇다.

※ 0205

졸업시ppt를 개인이 만들어 붙여야한다. 자바를 이용해서 썻다 등

13일부터 4일 정도 미니프로젝트 해보자
이번주 는 미니프로젝트

servers의 web.xml의 timeout을 
musthave web.xml에 붙여넣는다.

●06Session
F12 >application > Cookies >10-1:8000의 쿠키 삭제가능

★ %> 이유없이 빨간줄 오류가발생하면 jsp 종료했다 다시켜기
submit을 누르면  onsubmit을 1차실행 그다음 action실행

★★★ LoginProcess.jsp와 web.xml은 대소문자 일치시켜야한다.
만약 다를경우 web.xml을 기준으로 수정한다.

● MemberDTO.java ,  MemberDAO.java

ctlr + 클릭하면 해당 .js로 이동한다.
초보자들은 getStirng() 안에 이름그대로 넣을것

★★★ 06Session 외우기 자주사용 (xml에 내용 채워야한다.)
getRequestDispatcher 외우기
LoginForm.jsp 실행하고 로그인하고 나서 F12들어가서 쿠키 삭제하기
페이지 찾을수 없으면 서버(톰켓)이나sql 연결되어 있는지 확인하기
오류 : 부적합한 열이름 .sql 테이블이름 확인

프로세스는 내용필요없어서 <html>내용 지워도 상관없다.

● Common 파일 생성 , Link.jsp
페이징(어려운 기법 코드가 따로 있음)
103p
★ 액션태그(지금까지 배운건 예전에사용하던 코드)<br/>
자바빈 = DTO<br/>
★ page는 자주 사용하지 않는다.<br/>
● Person.java , 07ActionTag , UserBeanMain.jsp<br/>
★★★ jsp: 의  <br/>
★ post는 인코딩 안걸면 한글 깨진다.<br/>
★ id="person" 는 사용할 클래스명<br/>

★★★ \\304에서 받은 5. jsp\musthave_jsp-main\WebContent\WEB-INF web.xml 에서<br/>
<!-- post방식의 한글처리를 통합하는 내용 --> SetCharEncoding복사해서 <br/>
lib의 web.xml에 붙여넣어라<br/>
모델1방식 배워야하지만 해커가 조작이 가능함<br/>
JDBConnext.java의 세번째 생성자<br/>
Link.jsp 그대로 사용함<br/>

0206<br/>
실행이 안되면 처음부터 확인해야한다.<br/>
dbmanager부터<br/>
● 08Board , IsLoggedIn.jsp<br/>
getAttribute = 속성<br/>
 (주의사항 html5태그 중복 제거)<br/>
★★★★★★오라클 xe , orcl 둘다 설치하면 오류날수도 있다 server를 localhost로 바꾸어주자<br/>
selectView(num)의 쿼리문은 외우기<br/>
우리는 inner조인만 공부하면된다 inner조인만으로 다할수 있음<br/>
★★★

View.jsp<br/>
★★★ process는 html기능 필요없다 싹없애기 <br/>
String content = request.getParameter("content"); //Edit.jsp에서 넘어온 파라미터값 처리<br/>

출입금 만들기<br/>
일단 임시 jsp만들기<br/>
프로젝트 구상해보기<br/>

※ 0207
스프링으로 페이지 땡겨옴
★ 이클립스 코드에 오류있으면 Project탭 > clean
 ★09Board
페이징 기능은 리스트에서작업
sql은 자바에너어라(실습할때)

MustHave.sql 코드추가 
web.xml에서 "페이징 처리용 초기값 파라미터 설정" 추가, list.jsp 코드추가
 list.jsp > virtualNum = totalCount-- 주석처리
utils에 BoardPage.java 오타나면 안되니 가져다 붙여라
● EL(표현언어)
지금까지 해온건 2010년도에 유행했던거 EL이라는 것은 2010년도 이후에 출시된 언어
● 기본 사용법
★★★ 객체 표현방식 외우기
정적메소드 호출 해보기
오후 175p 까지
★★ JSP 166P 버전문제로 (integer) 안되니 99넣어서 실행할것
////////////////// 기타<br/>
1. xml에 정보가 제대로 입력되었는지 확인<br/>
98p 정적 쿼리문으로 회원 조회<br/>
100p 세션 (데이터 베이스연동되는 로그인 기능)<br/>
★★★★★★ 돈입출금, 입출금 기록 <br/>
Sessionmain까지 101<br/>


※ 0208
sql태그는 거의 안씀<br/>
★★★★★★ jstl사용하려면 jar파일 내려받아야한다.<br/>
크롬 > https://mvnrepository.com/ 1.2 > Files jar 버튼눌러 다운받아 lib파일에넣기<br/>
● set1.jsp > <%@ taglib prefix="c" uri="http://java.sun.com/jsp/jstl/core" %><br/>
자카르타는 10 버전이라 쓰면 안됨<br/>
jstl 5개 다 때려박으면 느려짐 필요한것만 붙여넣을것<br/>
★★ 복붙했고 철자틀리거 없는데 오류발생하면 jsp 닫았다 열어볼것<br/>

★★★★★★설날에 코드분석해보기<br/>
교재판매 폴더 jsp쇼핑몰pdf 공부하기<br/>
★ 189p까지<br/>
http://servlets.com/cos/ -> zip 파일을 다운 받음 <br/>
하단 Version : cos-22.05.zip 다운<br/>
cos-22.05 폴더 > lib > cos.jar을 이클립스의 lib폴더에 붙여넣기<br/>
★ 파일 업로드는 반드시 post방식을 사용한다.<br/>
MustHave.sql에 -- 파일 업로드용 데이터베이스 생성<br/>
★파일명이 중복된다. 대부분 연월분시일초를 파일명으로 한다. 그러면 중복될 가능성이 거의 없음<br/>
--오리지널 파일명으로 파일명이 길거나 한글이거나 확장자 포함<br/>
--저장용 파일명(중복배제용, 날짜나시간정보로 파일명을 생성)<br/>
●  MyfileDAO,DTO<br/>
● DBConnPool {//연결고장시 톰켓 서버의 server.xml과 context.xml을 확인하세요. (연결 실패시)<br/>
● UploadProcess.jsp<br/>
attachedFile은 첨부파일명<br/>
\은 주석처리되니 \\로 입력<br/>
진짜 서버에 올려야 보임216p까지<br/>

0213<br/>
MVC(MODEL, VIEW,v
13Servlet<br/>
정부에서 사업하는것 수원시청검색 > index.do do라는건 자바를 사용한다는 뜻<br/>
예외발생은 xml에서 만들수있다.<br/>
@WebServlet을 자주사용하는데 수정하려면 java파일을 일일이 찾아봐야한다.<br/>

● FrontController.jsp로 실행하면 URI,요청명 출력 안됨 href누르면 출력<br/>
인증방법 2가지방법 DB로 인증, 톰켓인증(서버관리자가 세팅할수있도록 만든거)<br/>
DB인증은 세션이용<br/>
톰켓은 application 이용<br/>
●  xml > <servlet-name>MemberAuth, MemberAuth.java<br/>
"admin_id"는 xml에서 복사하기<br/>
217p서블릿<br/>

수목금 미니프로젝트 쇼핑몰 선생님이 주셨던걸로<br/>
파일업로드 옮기기14MVCBoard<br/>
5.jsp 더미데이터, MVCFileBoard 참고해서 게시판 만들기<br/>
★ DAO에서 쿼리문 한줄로 쓸것<br/>



0213<br/>
MVC(MODEL, VIEW,<br/>
13Servlet<br/>
정부에서 사업하는것 수원시청검색 > index.do do라는건 자바를 사용한다는 뜻<br/>
예외발생은 xml에서 만들수있다.<br/>
@WebServlet을 자주사용하는데 수정하려면 java파일을 일일이 찾아봐야한다.<br/>

● FrontController.jsp로 실행하면 URI,요청명 출력 안됨 href누르면 출력<br/>
인증방법 2가지방법 DB로 인증, 톰켓인증(서버관리자가 세팅할수있도록 만든거)<br/>
DB인증은 세션이용<br/>
톰켓은 application 이용<br/>
●  xml > <servlet-name>MemberAuth, MemberAuth.java<br/>
"admin_id"는 xml에서 복사하기<br/>
217p서블릿<br/>

수목금 미니프로젝트 쇼핑몰 선생님이 주셨던걸로<br/>
파일업로드 옮기기14MVCBoard<br/>
5.jsp 더미데이터, MVCFileBoard 참고해서 게시판 만들기<br/>
★ DAO에서 쿼리문 한줄로 쓸것<br/>


★★★★★★★★★★★★★★★★★★★★★★★★★★★★★ 선생님<br/>
리퀘스트 영역에 대한 정리<br/>
:reuest개체를 가짐<br/>
클라이언트의 요청에 대해 같은 요청을 공유하는 페이지가 대응된다.<br/>
요청한 jsp페이지가 다른 jsp를 <jsp:include>하거나 <jsp:forward>하는 경우<br/>
이 두 페이지는 같은 요청 범위에 속하게 되어 같은 request 개체를 <br/>
공유하게 된다.<br/>
웹 브라우저가 요청을 할때마다 새로운 request개체가 생성됨.<br/>
-사용자가 요청했을 때 생성<br/>
-서버에서 요청에 대해 응답이 완료될때 소멸<br/>
-포워드 하는 순간에는 리퀘스트 영역이 그대로 유지(페이지 영역은 소멸)<br/>
★★★★★★★★★★★★★★★★★★★★★★★★★★★★★ end<br/>

미니프로젝트 빡세게 할필요없음<br/>
페이지, request , session 흐름만 패턴만, <br/>
DB설계 DTO 학생한명당 CRUD 게시판, 상품, 장바구니<br/>
테이블 5개정도<br/>

★예제따라하다 오류발생하면 View대문자확인, jsp의 do를 mit으로 통일할것<br/>

@WebServlet("/mvcboard/pass.mit") url에 요청 대문자일지는 내가 맞추는것<br/>

● 비밀번호 검증 256p<br/>


※ 0215<br/>
gitcmd교재 읽어보기 53p 보기<br/>
요즘은 인증키대신 토큰 사용함<br/>
new token classic<br/>
이클립스에서 머할거면 전부 체크해야 로그인된다.<br/>
암호까먹으면안됨 (ghp)<br/>
편집 > HTTPS, Personal Acces , 토큰 입력<br/>

이클립스 > 깃허브에서 jspProject 리포지토리 생성<br/>
ssh 코드복사 git@github.com:Woosangje/jspProject.git<br/>
Window > Open Perspective > git확인 > Clonse a git repository > https, 패스워드는 깃토큰<br/>
경로 찾아가기 어려우니 C:\git\jspProject로 단축시키기<br/>
MustHaveJSP우클릭 > team > Share project> finish<br/>
오른쪽 클릭 > team의 내용이 변경됐는지확인<br/>
window > Git Staging > 올리고싶은거 team>add to index > commit > configured는 하지말고 cancel입력할것<br/>
★ xml, sql은 올리지 말것<br/>
미니프로젝트 > 교재판매 폴더 쇼핑몰<br/>
조별로는 도와주는 수준으로 책에"북마켓" 적혀있는 곳만 제작하면된다.<br/>
취업은 스프링, 스프링부트로 해야한다. <br/>
(조팀명, 조원소개, 일정표, 순서도, UI기획서(화면설계서), ERD, 소스코드분석)<br/>
화면설계 https://yslab.kr/148<br/>

성공한 사람들은 왜 격무에도 스트레스가 없을까<br/>

북마크 페이지<br/>
48, 74, 109, 147, 188, 221, 260, 301, 341, 372, 403 434<br/>
468 494 539 583, 629, 655<br/>

processAddBook.jsp <br/>
 new MultipartRequest(request, realFolder, maxSize, encType, new DefaultFileRenamePolicy());<br/>
문제해결하기<br/>

0216<br/>
DTO 메뉴추가 삭제<br/>
제품 추가수정 삭제 관리자만 들어갈수 있도록 작성<br/>

★★★ db상의 문제인거같으면 톰켓 초기화 한다음 xml,꼭 수정해야한다.<br/>

★★★ 자바를 콘솔로 빌드싶다면 콘솔 빌드할main을 "Subway/src/main/java"<br/>
에서 생성하면 안된다.
★ ?, ?, ?  String, Int 잘 구별하기 ?붙이기 전에 sql코드를 붙여서 실행해보자.<br/>
★★ Exception으로 통합하기<br/>
conn.commit(); //DB 영구저장<br/>

jsp 쇼핑몰 303p까지<br/>
표만들기 정리를 쭉 해오기 mvc패턴 분석하기<br/>
폴더와 매칭해서 작업하기 context처리하는거 이해 엑셀로 정리<br/>

0219
받은 엑셀 시트 수정해보기<br/>
★ jsp form에서 DB insert시 한글 깨지면 xml에서 utf-8추가하기<br/>


※ 만약 버튼 조건문으로 제어하고 싶으면 143p참조<br/>
※ <textarea>정보</textarea> textarea사이에 엔터치면 안된다.<br/>
※ function deletePost(){}는 View.jsp에있다.<br/>

~jsp에서 ~jsp로 이동하고 ~java가 호출되는지<br/>

CondimentDAO.selectListPage > web.xml POST_PER_PAGE, PAGES_PER_BLOCK<br/>

157P 마저만들기<br/>

0221
"10.프로젝트 파일" 보기

리스트 포함 카트 참조 뱅크
의존성 빌드체크
뱅크 태그 클래스이름

발표 오전
AWS에 회원가입하기 해킹처럼오해되어서 학원에서 회원가입 해야한다.
핸드폰, 신용카드 인증
