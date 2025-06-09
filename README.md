
C-c C-c: 현재 top level form을 컴파일합니다. 주로 defun, defmacro등을 등록할때 사용.
C-x C-e: 현재 커서 바로 이전 expression을 실행(Evaluate)합니다. 디버깅할때 유용합니다.
C-M-x: 현재 top level form을 실행(Evaluate)합니다. 리턴값이 밑에 표시되고 한번에 입력할수 있기 때문에 많이 씁니다.
C-c C-z: REPL로 이동합니다. 이때 화면이 나눠지는데, C-x o로 양 창을 이동할수 있습니다.
TAB: 현재줄을 indent합니다. 여러줄을 입력할때 다음줄로 넘어갈때 항상 TAB를 눌러 주는게 좋습니다. 안그러면 자동 괄호 닫기 기능등이 비정상적으로 작동합니다.
C-j: 다음줄로 가서 indent합니다. Enter 누르고 TAB 누르는것과 같습니다. 익숙해지면 편하죠.
C-c C-q: 열린 괄호를 모두 닫습니다.
C-c M-q: 현재 form을 자동 indent합니다.
C-c C-k: 현재 파일을 컴파일&로드 합니다.
M-. : 해당 definition으로 이동
M-, : 이전으로 이동
C-c C-d h: 현재 단어를 hyperspec에서 찾아봅니다.
C-c TAB 또는 C-M-i : autocompletion. 누르면 창 나눠지면서 포커스 다른 창으로 이동하는데 여기서 C-n,C-p 등으로 원하는 단어 선택해서 Enter치면 완성되고, q를 누르면 취소됩니다.
C-c M-i : fuzzy autocompletion. with-output-file을 빨리 칠때 wof하고 C-c M-i치면 w*-o*-f*로 되어있는 거도 포함되어 선택할수 있습니다. 이게 원래 autocompletion보다 편해서 .emacs에서 디폴트로 변경해서 사용하고 있습니다.
C-M-n, C-M-p : expression 하나씩 앞뒤로 이동합니다. C-M-u은 상위로 이동합니다.
C-c Enter : Macro Expand-1. 매크로 짤때 필수죠.
여기까지가 에디터에서 사용하는 명령들이고, REPL에서도 에디터에서 사용할수 있는 단축키들이 대부분 그대로 통합니다. 추가적으로

Enter: Evaluate
C-Enter: 괄호 닫고 Evaluate
Shift-Enter: Eval하지 않고 다음줄로 내려갑니다.
C-↑, C-↓, M-p, M-n : 히스토리 기능
,q : SLIME 종료 (Swank도 종료)
다음은 디버깅 관련 단축키입니다.

C-Shift-i: inspect. 원하는 변수등에서 누르면 자세한 정보가 표시됩니다.
Ctrl-c Ctrl-t: trace. 원하는 함수이름에서 trace기능을 켜고 끌수 있습니다. trace 기능이 켜 있으면 해당 함수가 호출될때 인자와 리턴값이 표시됩니다. trace된 함수들을 모두 크기 위해서는 REPL에서 (untrace) 하면 됩니다.
실행(Evaluation)중 오류가 나면, 디버거가 뜹니다. 맨위에 오류가 설명되고, 그 밑에 재시작, 끝내기등 실행 재개에 대한 메뉴가 나옵니다. 왼쪽에 숫자를 입력하면 메뉴가 선택되지만, 숫자에 대한 메뉴가 일정하지 않기 때문에 다른 단축키를 알아두는게 좋습니다.

q: 종료 (quit)
0: 스택 한단계 위로 이동
밑에는 스택(Backtrace)이 표시되는데, 해당 라인으로 이동하여 Enter를 치면 자세한 내용이 표시됩니다.

M-n, M-p: 위/아래로 이동. 새로 이동한 줄의 자세한 내용이 표시되고 그전보던 줄의 자세한 내용은 감춰집니다.
v : 해당 스택 frame의 소스로 이동.
e : 해당 스택 frame에서 expression을 evaluate
i : 해당 스택 frame에서 expression을 inspect