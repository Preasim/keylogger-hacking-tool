# Xelogger
키로거 프로그램입니다. 사용자가 입력한 키값을 후킹하여 저장합니다.  

# Configuration
filemanager.py - 사용자 정의 함수입니다. 로그파일 이름 파싱, 로그파일 경로 파싱, 키 로깅, 파일사이즈 감지 등 파일에 관련된 기능을 담당합니다.  
winmanager.py - user32.dll 윈도우 라이브러리를 로드하여 사용자가 현재 활성화한 프로그램의 타이틀을 파싱하는 기능을 담당합니다.  
mailmanager.py - smtp 라이브러리를 사용합니다. 로그파일 사이즈가 20KB(20000B)가 될 경우 해당 로그파일을 읽어 공격자에게 로그를 전송합니다.
keylogger.py - Xelogger 프로그램의 메인 파일입니다.

# Requirement
Python 3.x.x (Python 3.9.1 버전에서 정상 작동 확인하였습니다.)  
pynput

# Usage
keylogger.py 파일을 실행하여 사용합니다.  
exe(실행파일)로 빌드하기 위해선 Pyinstaller 모듈을 사용합니다.  
pyinstaller --onefile --noconsole keylogger.py  

반드시 해당 프로젝트 파일을 다운로드 하신 뒤 mailmanager.py의 메일계정을 수정하여주시기 바랍니다.  
https://myaccount.google.com/lesssecureapps 해당 주소에 접속하셔서 반드시 보안 수준이 낮은 앱을 "사용" 으로 변경해주시기바랍니다.

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Xelogger
It's a keylogger program. Hooks and saves the user-entered key value.

# Configuration
filemanager.py - User-defined function. It is responsible for file-related functions such as parsing log file names, parsing log file paths, key logging, and file size detection.
winmanager.py - Load the user32.dll window library to parse the title of the program currently active by the user.
mailmanager.py - Use the smtp library. If the log file size is 20KB (20000B), read the log file and send the log to the attacker.
keylogger.py - This is the main file of the Xelogger.

# Requirement
Python 3.x.x (We checked normal operation in Python 3.9.1 version.)  
pynput

# Usage
Run and use the keylogger.py file.
Use the Pyinstaller module to build with exe (executable file).
pyinstaller --onefile --noconsole keylogger.py

Please make sure to download the project file and modify the email account on mailmanager.py.
Please access the address at https://myaccount.google.com/lesssecureapps and make sure to change the app to "Use" which is less secure.