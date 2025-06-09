
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
