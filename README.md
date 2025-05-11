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
* make dotest를 해서 cool 테스트 소스 파일이 출력되는 것을 확인한다. 

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


6. DARROW 규칙이 동작하는 것을 확인한다. 

* (Assignment1.pdf)[https://courses.edx.org/asset-v1:StanfordOnline+SOE.YCSCS1+3T2024+type@asset+block/PA1.pdf] 파일을 연다.
* 2 Introduction to Flex/JLex에서 Rule file의 구조 부분을 읽는다. 
* vscode에서 cool.flex 파일을 연다. 
* 다음 형식에 맞춰서 파일이 만들어져 있는 것을 확인한다.
```
%{
	C 문법에 따라 작성된 선언 
%}

특정 정규식에 이름 붙이기
DARROW		=>

%%

특정 정규식을 만족할 때 실행할 함수 정의
{DARROW}	{ return (DARROW); }

%%
C 문법에 따라 작성된 함수 (내용없음)
```
* vscode에서 PA2/cool-parse.h 파일을 연다. 
* `#define DARROW 272`를 확인한다.
* LX 터미널에서 cd ../을 입력해서 cool.flex가 있는 폴더로 이동한다.
* make lexer를 입력해서 컴파일한다.
* echo -e "=> => =>" > test2.cl을 입력해서 테스트 소스 파일을 만든다.
* ./lexer test2.cl을 입력해서 DARROW가 세번 출력되는지 확인한다. 


7. class 키워드에 대한 규칙을 추가한다. 
* (cool_manual.pdf)[https://courses.edx.org/asset-v1:StanfordOnline+SOE.YCSCS1+3T2024+type@asset+block/cool_manual.pdf] 파일을 연다. 
* cool_manual.pdf에서 10 Lexical Structure 안에 있는 10.4 Keywords에서 `class`가 키워드고 대소문자를 구분하지 않음을 확인한다. 
* (flex 메뉴얼)[https://westes.github.io/flex/manual/] 웹페이지의 6 Patterns를 읽는다.
* `{name}`이 name에 정의된 정규식을 쓴 것이라는 것을 확인한다.
* `(i:pattern)`이 대소문자에 관계없이 pattern을 적용하는 것임을 확인한다.
* PA2/cool-parse.h에서 `#define CLASS 258`를 읽는다.
* cool.flex의 `{DARROW} 	{ return (DARROW); }` 다음 줄에
  `(?i:class)		{ return (CLASS); }`를 입력한다.
* LX 터미널에서 make lexer를 입력해서 컴파일한다.
* echo -e "class =>" > test2.cl을 입력해서 테스트 소스 파일을 만든다.
* ./lexer test2.cl을 입력해서 CLASS와 DARROW가 출력되는지 확인한다. 


8. 공백 문자에 대한 규칙을 추가한다. 
* flex 메뉴얼의 4 Some Simple Examples에서 `[ \t\n]+ ` 규칙을 확인한다. 
* flex 메뉴얼의 6 Patterns에서 `'[xyz]' a character class, in this case, the pattern matches either an 'x', a 'y', or a 'z'`를 읽는다. 
* cool_manual.pdf의 10.5 White Space에서 공백 문자가 ' ', '\n', '\f', '\r', '\t', '\v'로 정해져 있음을 확인한다. 
* flex 메뉴얼의 6 Patterns에서 `'{name}' the expansion of the 'name' definition`을 읽는다. 
* cool.flex의 `DARROW	=>` 전 줄에 다음 코드를 추가한다.
```c
WHITESPACE		[ \n\f\r\t\v]
WHITESPACES		{WHITESPACE}+
```
* cool.flex의 `{DARROW} 	{ return (DARROW); }` 전전 줄에 `{WHITESPACES}		    `를 추가한다.
* LX 터미널에서 make lexer를 입력해서 컴파일한다.
* ./lexer test2.cl을 입력해서 CLASS와 DARROW가 출력되고 공백 문자는 출력되지 않는 것을 확인한다. 


9. 디버깅 규칙을 임시로 추가한다. 
* cool-lex.cc에서 lexer의 소스코드 중 다음과 같은 디버그 관련 내용을 읽는다. 
```c
/** The main scanner function which does all the work.
 */
YY_DECL
{
		if ( yy_flex_debug )
			{
			if ( yy_act == 0 )
				fprintf( stderr, "--scanner backing up\n" );
			else if ( yy_act < 4 )
				fprintf( stderr, "--accepting rule at line %ld (\"%s\")\n",
				         (long)yy_rule_linenum[yy_act], yytext );
			else if ( yy_act == 4 )
				fprintf( stderr, "--accepting default rule (\"%s\")\n",
				         yytext );
			else if ( yy_act == 5 )
				fprintf( stderr, "--(end of buffer or a NUL)\n" );
			else
				fprintf( stderr, "--EOF (start condition %d)\n", YY_START );
			}
}
```
* cool.flex의 `{WHITESPACES}		    ` 다음 줄에 `DEBUG 	{yy_flex_debug = 1;}`을 추가한다.
* LX 터미널에서 make lexer를 입력해서 컴파일한다.
* echo -e "DEBUG class =>" > test2.cl을 입력해서 테스트 소스 파일을 만든다.
* ./lexer test2.cl을 입력해서 디버깅 메시지들이 출력되는지 확인한다. 


10. 줄번호 관련 규칙을 추가한다. 
* lextest.cc의 main 함수에서 다음과 같은 출력 내용을 읽는다.
```c
int main(int argc, char** argv) {
	int token;

	while (optind < argc) {
	    fin = fopen(argv[optind], "r");
        curr_lineno = 1;

		cout << "#name \"" << argv[optind] << "\"" << endl;
	    
		while ((token = cool_yylex()) != 0) {
		dump_cool_token(cout, curr_lineno, token, cool_yylval);
	    }
	    
		fclose(fin);
	    optind++;
	}
	exit(0);
}
```
* cool.flex에서 `extern int curr_lineno;`를 확인한다. 
* cool.flex의 `{WHITESPACES}		    ` 전 줄에 `\n cur_lineno++;`을 추가한다.
* LX 터미널에서 make lexer를 입력해서 컴파일한다.
* echo -e "DEBUG class \n =>" > test2.cl을 입력해서 줄바꿈이 있는 테스트 소스 파일을 만든다.
* ./lexer test2.cl을 입력해서 줄바꿈 후에 줄번호가 바뀌어서 출력되는지 확인한다. 
* cat grading/
* ./lexer
* cd grading을 해서 grading 폴더로 이동한다. 
* ./143publicgrading PA2를 입력해서 채점을 시도한다. 

11. 다른 키워드들에 대한 규칙을 추가한다. 
* cool_manual.pdf에서 10 Lexical Structure 안에 있는 10.4 Keywords에서 다음과 같은 키워드 종류를 확인한다. 
`class`, `else`, `fi`, `if`, `in`, `inherits`, `isvoid`, `let`, `loop`, `pool`, `then`, `while`, `case`, `esac`, `new`, `of`, `not`, `true`, `false`. 
* `true`, `false`의 첫글자는 소문자여야 함을 확인한다.
* PA2/cool-parse.h에서 각각의 키워드에 대한 매크로 상수 정의를 다음과 같이 확인한다.
```c
#define CLASS 258
#define ELSE 259
#define FI 260
#define IF 261
#define IN 262
#define INHERITS 263
#define ISVOID 274
#define LET 264
#define LOOP 265
#define POOL 266
#define THEN 267
#define WHILE 268
#define CASE 269
#define ESAC 270
#define NEW 273
#define OF 271
#define NOT 281
#define BOOL_CONST 277
```
* flex 메뉴얼의 6 Patterns에서 `'rs' concatenation` 부분을 읽는다. 
* cool.flex의 `(?i:class)		{ return (CLASS); }` 다음 줄에 다른 키워드들에 대한 규칙을 다음과 같이 추가한다. 
```c
(?i:else)		{ return (ELSE); }
(?i:fi)			{ return (FI); }
(?i:if)			{ return (IF); }
(?i:in)			{ return (IN); }
(?i:inherits)	{ return (INHERITS); }
(?i:isvoid)		{ return (ISVOID); }
(?i:let)		{ return (LET); }
(?i:loop)		{ return (LOOP); }
(?i:pool)		{ return (POOL); }
(?i:then)		{ return (THEN); }
(?i:while)		{ return (WHILE); }
(?i:case)		{ return (CASE); }
(?i:esac)		{ return (ESAC); }
(?i:new)		{ return (NEW); }
(?i:of)			{ return (OF); }
(?i:not)		{ return (NOT); }
t(?i:rue)		{ return (BOOL_CONST); }
f(?i:alse)		{ return (BOOL_CONST); }
```
* LX 터미널에서 cd ..을 해서 소스파일이 있는 폴더로 이동한다. 
* make lexer를 해서 컴파일한다. 
* cat grading/keywords.cool을 해서 테스트 소스 파일 내용을 확인한다.
* ./lexer grading/keywords.cool을 입력해서 키워드가 인식되는지 확인한다. 
* ./cat grading/keywords.cool.out을 입력해서 정답에서는 true가 BOOL_CONST true로, false가 BOOL_CONST false로 출력되는 것을 확인한다.
* lextest.cc의 main 함수에서 출력 관련 내용을 읽는다.
```c
int main(int argc, char** argv) {
	    
		while ((token = cool_yylex()) != 0) {
			dump_cool_token(cout, curr_lineno, token, cool_yylval);
	    }
	    
	exit(0);
}
* utilities.cc의 dump_cool_token 함수에서 BOOL_CONST 관련 내용에서 전역변수 cool_yylval.boolean이 쓰임을 확인한다.
```c
void dump_cool_token(ostream& out, int lineno, int token, YYSTYPE yylval) {
	out << "#" << lineno << " " << cool_token_to_string(token);
	switch (token) {
		case (BOOL_CONST):
		out << (cool_yylval.boolean ? " true" : " false");
		break;
	}
}
```
* cool.flex의 `t(?:rue)		{ return (BOOL_CONST); }`를 `t(?:rue)		{ cool_yylval.boolean = true; }`로 변경한다.
* cool.flex의 `f(?:alse)	{ return (BOOL_CONST); }`를 `f(?:alse)		{ cool_yylval.boolean = false; }`로 변경한다.
* LX 터미널에서 make lexer를 입력해서 컴파일한다.
* ./lexer grading/keywords.cool을 입력해서 출력 내용을 확인한다. 
* ./cat grading/keywords.cool.out을 입력해서 정답이 출력 내용과 동일한 것을 확인한다.
* cd grading을 해서 폴더를 grading으로 바꾼다.
* ./143publicgrading PA2 를 입력해서 채점을 시도하고, 6/63점이 나온 것을 확인한다. 



12. 타입 이름과 객체 이름에 대한 규칙을 추가한다. 
* cool_manual.pdf에서 10 Lexical Structure 안에 있는 10.1 Integers, Identifiers, and Special Notation에서 타입 이름은 대문자로 시작하고, 객체 이름은 소문자로 시작하고, 두번째 문자부터는 대소문자, 숫자, 밑줄이 쓰일 수 있음을 확인한다.
* flex 메뉴얼의 6 Patterns에서 `'r|s' either an 'r' or an 's'`를 읽는다. 
* cool.flex의 `WHITESPACES		{WHITESPACE}+` 다음줄에 다음 코드를 추가한다.
```c
LETTER_UPPER	[A-Z]
LETTER_LOWER	[a-z]
LETTER			{LETTER_UPPER}|{LETTER_LOWER}
LETTER_OR_DIGIT	{LETTER}|{DIGIT}
TYPEID			{LETTER_UPPER}{LETTER_OR_DIGIT}*
OBJECTID		{LETTER_LOWER}{LETTER_OR_DIGIT}*		
```

* PA2/cool-parse.h에서 각각의 이름과 에러에 대한 매크로 상수 정의를 다음과 같이 확인한다.
```c
#define TYPEID 278
#define OBJECTID 279
#define ERROR 283
```
* flex 메뉴얼의 6 Patterns에서 `'.' any character`를 읽는다. 
* flex 메뉴얼의 7 How the Input Is Matched에서 가장 긴 길이의 패턴이 매칭되고, 같은 길이의 패턴이 매칭되면 먼저 나온 규칙에 따라 처리됨을 확인한다.
* cool.flex의 `f(?:alse)		{ cool_yylval.boolean = false; }` 다음 줄에 이름에 대한 규칙을 다음과 같이 추가한다. 
```c
{TYPEID}	{ return (TYPEID); }
{OBJECTID}	{ return (OBJECTID); }
.			{ return (ERROR); }
```
* cool.flex의 규칙 중 마지막 줄에 에러에 대한 규칙을 다음과 같이 추가한다. 
```c
``` 
* LX 터미널에서 cd ..을 해서 소스파일이 있는 폴더로 이동한다. 
* make lexer를 해서 컴파일한다. 
* cat grading/objectid.test.cool을 해서 테스트 소스 파일 내용을 확인한다.
* ./lexer grading/objectid.test.cool을 입력해서 이름이 인식되는지 확인한다. 
* ./cat grading/keywords.cool.out을 입력해서 정답에서는 true가 BOOL_CONST true로, false가 BOOL_CONST false로 출력되는 것을 확인한다.
* lextest.cc의 main 함수에서 출력 관련 내용을 읽는다.
```c
int main(int argc, char** argv) {
	    
		while ((token = cool_yylex()) != 0) {
			dump_cool_token(cout, curr_lineno, token, cool_yylval);
	    }
	    
	exit(0);
}
* utilities.cc의 dump_cool_token 함수에서 BOOL_CONST 관련 내용에서 전역변수 cool_yylval.boolean이 쓰임을 확인한다.
```c
void dump_cool_token(ostream& out, int lineno, int token, YYSTYPE yylval) {
	out << "#" << lineno << " " << cool_token_to_string(token);
	switch (token) {
		case (BOOL_CONST):
		out << (cool_yylval.boolean ? " true" : " false");
		break;
	}
}
```
* cool.flex의 `t(?:rue)		{ return (BOOL_CONST); }`를 `t(?:rue)		{ cool_yylval.boolean = true; }`로 변경한다.
* cool.flex의 `f(?:alse)	{ return (BOOL_CONST); }`를 `f(?:alse)		{ cool_yylval.boolean = false; }`로 변경한다.
* LX 터미널에서 make lexer를 입력해서 컴파일한다.
* ./lexer grading/keywords.cool을 입력해서 출력 내용을 확인한다. 
* ./cat grading/keywords.cool.out을 입력해서 정답이 출력 내용과 동일한 것을 확인한다.
* cd grading을 해서 폴더를 grading으로 바꾼다.
* ./143publicgrading PA2 를 입력해서 채점을 시도하고, 6/63점이 나온 것을 확인한다. 










00. 정수 상수 규칙을 추가한다.

* cool-parse.h에서 `#define INT_CONST 276`을 확인한다. 
* Assignment1.pdf에서 `\DIGIT	[0-9]` 앞뒤 문단을 읽는다. 
* cool.flex에서 `DARROW		=>` 다음 줄에 `DIGIT	[0-9]`를 입력한다.
* cool_manual.pdf에서 10 Lexical Structure 안에 있는 10.1 Integers, Identifiers, and Special Notation을 읽는다. 

* cool.flex에서 `DIGIT		[0-9]` 다음 줄에 `DIGITS		{DIGIT}+`를 입력한다.
* Assignment1.pdf에서
```c
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

```c
/** the current token.
 * 
 */
extern char *yytext;
#define yytext_ptr yytext

/* yy_hold_char holds the character lost when yytext is formed. */
static char yy_hold_char;

/* Points to current character in buffer. */
static char *yy_c_buf_p = (char *) 0;
static int yy_init = 0;		/* whether we need to initialize */
static int yy_start = 0;	/* start state number */

/* Done after the current pattern has been matched and before the
 * corresponding action - sets up yytext.
 */
#define YY_DO_BEFORE_ACTION \
	(yytext_ptr) = yy_bp; \
	yyleng = (size_t) (yy_cp - yy_bp); \
	(yy_hold_char) = *yy_cp; \
	*yy_cp = '\0'; \
	(yy_c_buf_p) = yy_cp;

static void yy_load_buffer_state(void) {
	yytext_ptr = yy_c_buf_p = YY_CURRENT_BUFFER_LVALUE->yy_buf_pos;
	yyin = YY_CURRENT_BUFFER_LVALUE->yy_input_file;
	yy_hold_char = *(yy_c_buf_p);
}

/** The main scanner function which does all the work.
 */
int cool_yylex(void) {
	yy_state_type yy_current_state;
	char *yy_cp, *yy_bp;

	if (!yy_init) {
		yy_init = 1;
		if (!yy_start) 
			yy_start = 1;	/* first start state */
		yy_load_buffer_state();
	}
	
	while(1) {
		yy_bp = yy_cp = yy_c_buf_p;
		*yy_cp = yy_hold_char;
		yy_current_state = yy_start;

	yy_match:
		do {
			yy_current_state = yy_nxt[yy_base[yy_current_state] + yy_ec[*yy_cp]];
			++yy_cp;
		} while( yy_base[yy_current_state] != 7);

		YY_DO_BEFORE_ACTION;

		/* cool.flex 내용 */
		case 1:
		{ return (DARROW); }
	}
}
```

* cool-parse.h에서 yytokentype에 `INT_CONST`가 있는 것을 확인한다. 
* cool.flex의 `{DARROW} 	{ return (DARROW); }` 다음 줄에 다음 코드를 추가한다.
```c
{DIGITS} {
	cool_yylval.symbol = inttable.add_string(yytext);
	return INT_CONST;
}
```
* LX 터미널에서 cd ../을 입력해서 cool.flex가 있는 폴더로 이동한다.
* make lexer를 입력해서 컴파일한다.
* echo -e "0 123 =>" > test2.cl을 입력해서 소스 파일을 만든다.
* ./lexer test2.cl을 입력해서 INT_CONST와 DARROW가 출력되는지 확인한다. 
* cd grading을 해서 grading 폴더로 이동한다. 
* ./143publicgrading PA2 를 입력해서 채점을 시도하고, 5/63점이 나온 것을 확인한다. 



