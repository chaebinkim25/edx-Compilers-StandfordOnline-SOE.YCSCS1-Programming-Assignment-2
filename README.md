# edX. Compilers. SOE.YCSCS1 첫번째 프로그래밍 과제

## [작업 환경 설정](https://courses.edx.org/courses/course-v1:StanfordOnline+SOE.YCSCS1+3T2020/7b74698308574f3c89d2ed498f26a019/?_gl=1*f2m4io*_ga*MzM1NDMxMDE3LjE2NTA2NDkzNTI.*_ga_D3KS4KMDT0*MTY4MjYyODk4OC4xNC4xLjE2ODI2MjkxNDYuMC4wLjA.)

1. VirtualBox를 다운로드하고 설치한다. 
2. 강의 VM을 다운로드하고 압축을 푼다. 
3. VirtualBox에서 강의 VM을 설정한다. 

* VirtualBox를 실행한다.
* 실행된 Oracle VirtualBox 관리자에서 추가 버튼을 클릭한다.
* 강의 VM 압축을 푼 폴더에서 Compilers 폴더로 들어간다.
* Copilers 파일 선택하고 열기 버튼을 클릭한다.
* Oracle VirtualBox 관리자에 새로 추가된 Compilers를 클릭한다.
* 설정 버튼을 클릭한다.
* 공유 폴더 메뉴를 클릭한다.
* 오른쪽에 있는 폴더+ 버튼을 클릭한다.
* 폴더 경로 오른쪽의 꺽쇠를 클릭해서 드롭다운 메뉴를 펼친다.
* 기타 메뉴를 클릭한다.
* 작업 폴더를 새로 만들고, 폴더 선택을 클릭한다.
* 폴더 이름을 cool_로 설정한다.
* 마운트 지점에 ~/share를 입력한다.
* 자동 마운트를 클릭해서 체크한다.
* 확인 버튼을 클릭해서 공유 추가를 완료한다.
* 확인 버튼을 클릭해서 설정을 완료한다.
* Oracle VirtualBox 관리자에서 시작 버튼을 클릭한다.
* 부팅 메뉴에서 첫번째 항목 Bodhi Linux를 선택한다.
* LX 터미널 아이콘을 클릭해서 LX 터미널을 연다. 
* Oracle VirtualBox 관리자에서 저장소의 [광학 드라이브] VBoxAdditions.iso를 클릭한다. 
* Choose/Create a Disk Image 메뉴를 클릭한다.
* 가상크기와 실제크기가 58MB인 VBoxGuestAdditions.iso를 클릭한다.
* 선택 버튼을 클릭해서 디스크를 삽입한다. 
* Compilers[실행 중] - Oracle Virtual box 창을 클릭해서 다시 실행중인 가상머신으로 돌아온다. 
* LX 터미널에서 cd /dev 입력해서 장치들이 있는 폴더로 이동한다.
* ls를 입력해서 장치들 중에 cdrom이 있는지 확인한다.
* sudo mount /dev/cdrom /mnt 라고 입력해서 cdrom 내용을 /mnt 폴더에 연결시킨다.
* cd /mnt를 해서 cdrom 내용이 있는 폴더로 이동한다.
* ls로 내용을 확인한다.
* sudo ./VBoxLinuxAdditions.run으로 설치를 시작한다.
* 설치가 끝나면, sudo reboot 를 입력해서 가상머신을 재시작한다.
* LX 터미널 아이콘 클릭해서 LX 터미널을 연다.
* ls로 홈 폴더의 내용을 확인한다.
* cool 폴더 말고 다른 폴더가 있으면 (~share와 같은 폴더) rmdir 폴더이름을 입력해서 삭제한다.
* mkdir ~/share 로 공유 폴더를 만든다.
* sudo mount -t vboxsf cool_ ~/share 로 공유폴더 공유를 시작한다.
* cd ~/cool로 강의 폴더로 이동한다.
* ls로 내용 확인한다.
* cd assignments로 과제 폴더로 이동한다.
* ls로 내용 확인한다.
* cp PA2/* ~/share 로 이번에 할 과제 폴더의 모든 내용을 공유폴더에  복사하기
* 윈도우에서 공유 폴더가 연결된 작업 폴더를 열고 README, cool.flex.SKEL 등의 파일이 있는지 확인한다.
* vscode에서 작업폴더를 연다.
* test.cl.SKEL 파일 이름을 test.cl로 바꾼다.
* cool.flex.SKEL 파일 이름을 cool.flex로 바꾼다.

4. 빌드를 테스트한다. 

* LX 터미널에서 cd ~/cool 입력해서 강의 폴더로 이동한다.
* ls로 내용을 확인한다.
* cd src로 소스 파일 폴더로 이동한다.
* ls로 내용을 확인한다.
* cp PA2/* ~/share 로 소스 파일들을 복사한다.
* cd ~/cool 로 강의 폴더로 이동한다. 
* ls로 내용을 확인한다. 
* cd include로 헤더 파일 폴더로 이동한다.
* ls로 내용을 확인한다. 
* cp -r PA2 ~/share 로 헤더 파일들을 폴더째로 폭사한다. 
* cd ~/share 로 공유 폴더로 이동한다.
* ls로 내용 확인한다.
* make lexer로 빌드한다.
* ls로 내용 확인하고, lexer가 있는지 본다.

5. 채점 스크립트 실행을 테스트한다. 

* (강의의 과제 페이지에 있는 링크)[https://courses.edx.org/asset-v1:StanfordOnline+SOE.YCSCS1+3T2024+type@asset+block/pa1-grading.pl]를 클릭해서 채점 스크립트 소스 파일을 연다. 
* 화면 가운데를 한번 클릭하고, Ctrl + A 키를 입력해서 전체선택한다.
* Ctrl + C 키로 복사한다. 
* vscode에서 이름이 pa1-grading.pl인인 파일을 만든다. 
* Ctrl + V 키로 붙여넣기 한다.
* LX 터미널에서 ./pa1-grading.p1로 스크립트를 실행한다. 
* ls를 입력해서 grading 폴더가 만들어졌는지 확인한다. 
* cd grading을 해서 grading 폴더로 이동한다. 
* ls로 내용을 확인한다. 
* ./143publicgrading PA2 를 입력해서 채점을 시도하고, 5/63점이 나온 것을 확인한다. 

6. 

* (Assignment1.pdf)[https://courses.edx.org/asset-v1:StanfordOnline+SOE.YCSCS1+3T2024+type@asset+block/PA1.pdf] 파일을 연다.
* 2 Introduction to Flex/JLex에서 Rule file의 구조 부분을 읽는다. 
* vscode에서 cool.flex 파일을 연다. 
* 다음 형식에 맞춰서 파일이 만들어져 있는 것을 확인한다.
```
%{
	C 문법에 따라 작성된 선언 
%}
특정 정규식에 이름 붙이기 (=>에 DAROOW라는 이름이 붙여져 있다.)
%%
특정 정규식을 만족할 때 실행할 함수 정의 (DARROW 정규식을 만족할 경우, C에 정의된 DARROW를 반환한다.)
%%
C 문법에 따라 작성된 함수 (내용없음)
```
* vscode에서 PA2/cool-parse.h 파일을 연다. 
* `#define DARROW 272`와 `#define INT_CONST 276`을 확인한다. 
* Assignment1.pdf에서 `\DIGIT	[0-9]` 앞뒤 문단을 읽는다. 
* cool.flex에서 `DARROW		=>` 다음 줄에 `DIGIT	[0-9]`를 입력한다.
* (cool_manual.pdf)[https://courses.edx.org/asset-v1:StanfordOnline+SOE.YCSCS1+3T2024+type@asset+block/cool_manual.pdf] 파일을 연다. 
* cool_manual.pdf에서 10 Lexical Structure 안에 있는 10.1 Integers, Identifiers, and Special Notation을 읽는다. 
* cool.flex에서 `DIGIT		[0-9]` 다음 줄에 `DIGITS		DIGIT+`를 입력한다.
* Assignment1.pdf에서
```
{DIGIT} {
	cool_yylval.symbol = inttable.add_string(yytext);
	return DIGIT_TOKEN;
}
```
의 앞뒤 문단을 읽는다. 
* cool.flex에서 `cool_yylval`의 타입이 `YYSTYPE`임을 확인한다.
* PA2/cool-parse.h에서 `YYSTYPE`이 union이고, `Symbol symbol`이 요소임을 확인한다. 
* PA2/cool-parse.h에서 `Symbol` 타입이 `Entry*` 타입임을 확인한다. 
* PA2/stringtab.h에서 `inttable`의 타입이 `IntTable`임을 확인한다.
* `IntTable`은 `StringTable<IntEntry>`를 상속받은 클래스임을 확인한다.
* `template <class Elem> class StringTable`에 `Elem *add_string(char *s)`가 있음을 확인한다. 
* `IntEntry`는 `Entry`를 상속받은 클래스임을 확인한다.
* cool-lex.cc에서 `yytext`의 값이 다음과 같이 쓰이고 있음을 확인한다.
```
extern char *yytext;
#define yytext_ptr yytext
int cool_yylex(void)
{
	yy_state_type yy_current_state;
	char *yy_cp, *yy_bp;
}
```
