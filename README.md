# 서울대학교 학위논문 LaTeX 템플릿 (한글 논문)

서울대학교 학위논문을 LaTeX를 이용하여 우리말로 작성할 때 사용하는 템플릿입니다. 참고로 학교 도서관에서는 학위논문 예시 doc, hwp 파일을 제공하나 이 양식을 그대로 쓸 필요는 없다고 했으며, LaTeX로 작성된 예시 코드는 제공하지 않습니다.

한국어 참고문헌와 영어 참고문헌을 함께 쓰는 국문 학위논문의 특성상 한국어와 영어 참고문헌을 자동으로 처리하기 위해 한국텍학회 https://www.ktug.org 의 noname님 도움을 많이 받았습니다. 이 LaTeX 템플릿에서는 참고문헌 처리를 위해 biber를 사용합니다.

references.bib에서 한국어 참고문헌에만 keywords={kobib} 을 추가하시면 biber가 본문에서 언급한 참고문헌만 추려서 한글, 영어 논문을 자동으로 참조하여 작성합니다.

기본적인 템플릿은 https://www.overleaf.com/latex/templates/snu-dissertation-template/fxvtwvxzdpvp 을 사용하였고, 우리말 학위논문에 맞게 세부적인 부분을 모두 고쳤습니다.

제가 작성한 학위논문 내용의 일부를 예시로 넣었으니 작성자의 의도에 맞게 고쳐 쓰시길 바랍니다.

# 사용법

1. MikTeX를 설치합니다.
2. MikTeX Console을 실행한 후, Check for updates를 눌러서 모든 패키지를 업데이트합니다.
3. Visual Studio Code를 설치합니다.
4. 확장 기능으로 Korean Language Pack과 LaTeX Workshop을 설치합니다.
5. settings.json.7z 압축 파일을 풀어서 settings.json 파일을 C:\Users\계정이름\AppData\Roaming\Code\User 에 붙여 넣습니다.
6. Visual Studio Code를 실행하여 사이드바의 LaTeX를 누른 후, LaTeX 프로젝트에서 레시피:xelaex -> biber -> xelatex 가 나오는지 확인합니다.
7. 논문을 작성한 후, LaTeX 프로젝트에서 레시피:xelaex -> biber -> xelatex 로 컴파일합니다.
8. 잘 되면 중간중간 MikTeX Console에서 없는 패키지를 실시간으로 내려받아 설치할 것입니다. 긍정적인 답변을 클릭합니다.

# 작성 팁

Visual Studio Code와 GitHub Copilot을 연동하면 번거로운 표나 반복되는 형태의 문장을 작성하는 데에 큰 도움을 받을 수 있습니다.

LaTeX PDF 보기에서 tex 파일에서 커서를 두고 Ctrl + Alt + J를 누르면 PDF 상의 해당 부분으로 가고, PDF에서는 Ctrl + 마우스 왼쪽 버튼 더블 클릭 하면 tex 파일의 해당 부분으로 이동됩니다.

manuscript.tex로부터 title.tex와 /chaps 안에 있는 tex 파일이 붙는 구조입니다.

목차의 수준은 manuscript.tex의 \setcounter{tocdepth}{2} % 차례에 출력할 목차의 깊이 (2는 subsection까지, 3은 subsubection까지) 부분을 참고하여 정할 수 있습니다.

# 한계

2024년 겨울 기준으로 MacOS에서는 MikTeX에서 일부 라이브러리가 작동하지 않아 사용할 수 없었습니다. 윈도우에서는 잘 작동했습니다.
