# 서울대학교 학위논문 LaTeX 템플릿 (한글 논문)

서울대학교 학위논문을 LaTeX를 이용하여 우리말로 작성할 때 사용하는 템플릿입니다. 참고로 학교 도서관에서는 학위논문 예시 doc, hwp 파일을 제공하나 이 양식을 그대로 쓸 필요는 없다고 했으며, LaTeX로 작성된 예시 코드는 제공하지 않습니다.

한국어 참고문헌와 영어 참고문헌을 함께 쓰는 국문 학위논문의 특성상 한국어와 영어 참고문헌을 자동으로 처리하기 위해 한국텍학회 https://www.ktug.org 의 noname님 도움을 많이 받았습니다. 이 LaTeX 템플릿에서는 참고문헌 처리를 위해 biber를 사용합니다.

references.bib에서 한국어 참고문헌에만 keywords={kobib} 을 추가하시면 biber가 본문에서 언급한 참고문헌만 추려서 한글, 영어 논문을 자동으로 참조하여 작성합니다.

기본적인 템플릿은 https://www.overleaf.com/latex/templates/snu-dissertation-template/fxvtwvxzdpvp 을 사용하였고, 우리말 학위논문에 맞게 세부적인 부분을 모두 고쳤습니다.

제가 작성한 학위논문 내용의 일부를 예시로 넣었으니 작성자의 의도에 맞게 고쳐 쓰시길 바랍니다. LaTeX를 이용하여 한국어로 학위 논문 작성 시 이 파일을 얼마든지 변형해서 사용하실 수 있습니다.

# GitHub에서 학위논문 LaTeX 템플릿 다운로드

1. 편집할 파일을 내려 받을 디렉토리로 이동합니다.
2. git clone https://github.com/kungmo/SNU_Dissertation_LaTeX_Korean.git 을 실행하여 템플릿을 통째로 내려 받습니다.
3. SNU_Dissertation_LaTeX_Korean 이라는 디렉토리에 파일이 모두 다운로드될 것입니다.

# 글꼴 설치

1. SNU_Dissertation_LaTeX_Korean 디렉토리 안에 Fonts라는 이름으로 디렉토리를 만듭니다.
2. Fonts_to_install.7z.001과 Fonts_to_install.7z.002를 방금 만든 Fonts 디렉토리에 넣습니다.
- 2026년 1월 업데이트: 윈도우와 리눅스, 맥OS에서 모두 작동하도록 글꼴을 Fonts 디렉토리를 만들어서 모두 집어 넣고, manuscript.tex에 글꼴의 파일명을 명시했습니다. 운영체제마다 글꼴을 처리하는 방법이 매우 다르기 때문에 Font 디렉토리 안에 있는 글꼴 파일의 이름을 지정하는 방법을 적용했습니다.
3. 7-zip으로 컴파일에 필요한 글꼴인 함초롬체 LVT와 Tex Gyre를 Fonts에 풀어줍니다. 2025년 2월 기준으로 한국텍학회 https://www.ktug.org 웹 사이트가 작동하지 않아 링크를 걸지 못 하고 GitHub에 글꼴을 업로드했습니다.
2026년 1월에도 한국텍학회 웹사이트가 복구되지 않아 부득이하게 글꼴 파일을 유지합니다.

# 사용법

1. MikTeX(윈도우, 리눅스)나 MacTeX(맥OS) 설치합니다.
- 윈도우, Linux: https://miktex.org/download 를 참고하여 설치합니다.
- 맥OS: https://www.tug.org/mactex/mactex-download.html 를 참고하여 설치합니다.
2. 설치한 MikTeX나 MacTeX를 업데이트합니다.
- 윈도우, 리눅스: MikTeX Console을 실행한 후, Check for updates를 눌러서 모든 패키지를 업데이트합니다.
- 맥OS: 터미널을 열고 sudo tlmgr update --self 를 실행합니다.
3. Visual Studio Code를 설치합니다.
4. 확장 기능으로 Korean Language Pack과 LaTeX Workshop을 설치합니다.
5. settings.json.7z 압축 파일을 풀어서 settings.json 파일을 열고
- editor.fontFamily에서 VSCode에서 쓸 글꼴의 종류를 설정합니다.
- editor.fontSize에서 VSCode에서 쓸 글꼴의 크기를 설정합니다.
6. 손본 settings.json 파일을
- 윈도우: C:\Users\계정이름\AppData\Roaming\Code\User 에 붙여 넣습니다.
- 리눅스: /home/계정이름/.config/Code/User 에 붙여 넣습니다.
- 맥OS: /Users/계정이름/Library/Application Support/Code/User 에 붙여 넣습니다.
6. Visual Studio Code를 실행하여 사이드바의 LaTeX를 누른 후, LaTeX 프로젝트에서 레시피:xelaex -> biber -> xelatex 가 나오는지 확인합니다.
7. 논문을 작성한 후, LaTeX 프로젝트에서 레시피:xelaex -> biber -> xelatex 로 컴파일합니다.
8. 윈도우, 리눅스: 잘 되면 중간중간 MikTeX Console에서 없는 패키지를 실시간으로 내려받아 설치할 것입니다. 뭔가 설치하겠다는 메시지가 나오면 긍정적인 답변을 클릭합니다.
맥OS: 없는 패키지는 TeX Live Utility를 실행하여 검색하고 설치합니다.

# 작성 팁

1. Visual Studio Code와 GitHub Copilot을 연동하면 번거로운 표나 반복되는 형태의 문장을 작성하는 데에 큰 도움을 받을 수 있습니다.
2. LaTeX PDF 보기에서 tex 파일에서 커서를 두고 Ctrl + Alt + J를 누르면 PDF 상의 해당 부분으로 가고, PDF에서는 Ctrl + 마우스 왼쪽 버튼 더블 클릭 하면 tex 파일의 해당 부분으로 이동됩니다.
3. manuscript.tex로부터 title.tex와 /chaps 안에 있는 tex 파일이 붙는 구조입니다.
4. 목차의 수준은 manuscript.tex의 \setcounter{tocdepth}{2} % 차례에 출력할 목차의 깊이 (2는 subsection까지, 3은 subsubection까지) 부분을 참고하여 정할 수 있습니다.

# 컴파일 시 오류 대처법

1. 윈도우: Perl이 설치되어 있지 않다고 나오면 터미널을 실행한 후, winget install -e --id StrawberryPerl.StrawberryPerl 을 실행하여 Strawberry Perl을 설치하세요.
2. 글꼴을 설치했는데도 Tex Gyre Termes 등의 글꼴이 설치되어 있지 않다고 하면 VSCode를 종료한 다음 MikTex Console을 별도로 실행시킨 다음 Packages에서 'gyre'로 검색하여 나오는 'tex-gyre'와 'tex-gyre-math'를 설치하면 글꼴 인식 문제를 해결할 수 있습니다.
3. 맥OS의 경우 글꼴을 못 찾는다고 하면 터미널을 열고
- ln -s /Library/TeX/Root/texmf-dist/fonts/opentype ~/Library/Fonts/opentype
- ln -s /Library/TeX/Root/texmf-dist/fonts/truetype ~/Library/Fonts/truetype
를 실행해 보십시오.

# 한계

2026년 1월 기준으로 MacOS에서는 MikTeX에서는 여전히 일부 라이브러리가 작동하지 않아 사용할 수 없었고, Apple Silicon을 지원하지 않고 있어서 맥OS에서는 MacTeX를 설치해야 했습니다.
