# 제 13강 foreground와 background 프로세스
## 쉘 사용법 정리 - 리눅스 프로세스 
### 프로세스 vs 바이너리 
- 코드 이미지 또는 바이너리 : 실행파일
- 실행중인 프로그램: 프로세스 
  - 가상 메모리 및 물리 메모리 정보 
  - 시스템 리소스 관련 정보 
  - 스케줄링 단위 

---
## 리눅스는 다양한 프로세스 실행 환경  
- 리눅스는 기본적으로 다양한 프로세스가 실행됨 
  - 유닉스 철학: 여러 프로그램이 서로 유기적으로 각자의 일을 수행하면서 전체 시스템이 동작하도록 하는 모델 

---
## foreground process/ background process
- foreground process: 쉘(shell)에서 해당 프로세스 실행을 명령한 후 해당 프로세스 수행 종료까지 사용자가 다른 입력을 하지 못하는 프로세스 

- background process: 사용자 입력과 상관없이 실행되는 프로세스 
  - 쉘(shell)에서 해당 프로세스 실행 시, 맨 뒤에 **&** 을 붙여줌
  - 사용 예 
  ```
  # 루트 디렉토리 밑에 py의 확장자를 가진 모든 파일의 출력스트림을 background process로 list.txt에 담는다
  $ find / -name '*.py' > list.txt &
  ```  