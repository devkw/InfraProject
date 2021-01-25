# InfraProject
- 노가다 시간 줄이기 위한 자동화 스크립트
- 인프라진단 스크립트 실행 후 텍스트 결과물을 엑셀로 복사하는 시간을 줄이기 위해 만들었습니다.
- 핵심은 선택된 폴더의 텍스트 파일을 모두 파싱하여 지정된 엑셀의 셀에 자동으로 입력해줍니다.

- pyinstaller를 활용하여 exe파일로 배포하려했는데 실패하였습니다. ㅠ
- 혹시 성공하신 분은 알려주시면 감사하겠습니다.

# 설치
스크립트를 실행하려면 파이썬3가 설치되어있어야하며 사용되는 라이브러리를 모두 설치해주셔야합니다.

```
git clone https://github.com/bbakbbak2/InfraProject.git
pip install pyqt5
pip install openpyxl
pip install configparser
```

# 준비사항
1. 사용하시는 쉘 스크립트 파일(windows.bat, linux.sh)에 원하시는 파싱부분에 파싱문자열을 입력하셔야합니다.
2. 수정된 스크립트를 실행하면 결과물 텍스트 파일에 파싱 문자열이 같이 기록될 것입니다.
3. InfraProject 스크립트를 실행하여 입력하신 파싱문자열을 기반으로 내용을 복사하게 됩니다. 
4. 작업전 원본 엑셀은 백업해두시기 바랍니다.

# 파일
- main.py: GUI를 구현한 코드입니다.
- parsing.py: 파싱코드 존재합니다.
- config.ini : 현재 설정을 저장하고 재사용할 수 있습니다.
- samples : 테스트용, 텍스트 결과물입니다.
- hello.xlsx : 테스트용, 엑셀 파일입니다.

# 실행
```
python main.py
```

# 메뉴내용
1. 엑셀파일 선택: 결과물을 입력할 엑셀 파일을 선택합니다.
2. 텍스트 디렉토리 선택: 결과물 텍스트 파일들을 한곳에 모아두어서 지정하는 것이 좋습니다.
3. 파싱시작/종료 문자열: 핵심이 되는 부분입니다. 파싱을 위해 텍스트 결과물에 해당 문자열이 존재해야합니다.
4. 셀 위치 열/행: 첫 시작 열과 행을 조절 할 수 있습니다.
5. 셀 너비/높이: 너비와 높이를 지정할 수 있습니다.
