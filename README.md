# OpenSW01

**1) 유닉스 리눅스 명령어(top)**
- 시스템의 프로세스/메모리 사용 상태를 5초 간격으로 업데이트 하여 출력
- 화면에 출력되는 기본값은 현재시간, 시스템 업데이트 시간, 시스템에 로그인한 사용자 수, 지난 1분/5분/15분간의 시스템 평균 부하 출력
- 프로세스 정보, CPU 상태, 메모리와 스왑 상태 출력


***top [옵션]***


- -b : 배치모드로 정보 출력, 실시간 상화 대화형모드로 정보를 화면에 일렬로 출력
- -d delay : 지정한 시간의 간격으로 정보 업데이트하여 출력
- -i idle : 토글값이 off일 때, idle 프로세스나 좀비 프로세스 정보를 출력하지 않음
- -n num : 지정한 시간만큼 업데이트 정보 츨력
- -p pid : 지정한 프로세스 ID의 정보 출력
- -q : 시간의 간격 없이 계속하여 업데이트 정보 출력
- -s : 몇 개의 대화식 명령 비활성화(시큐어 모드)
- -S : 누적된 정보 출력(cumulative 모드)


*top 단축키 명령어*


|명령어|설명|
|------|---|
|space|정보 업데이트|
|^L|스크린 초기화|
|F or f|필드 추가&제거|
|O or o|출력하는 피드 정렬 순서 변경|
|h or ?|사용 가능한 명령어 출력|
|k|프로세스 종료|
|n or #|출력할 프로세스 수 지정|
|s|출력할 정보 업데이트 시간 지정|
|W|~/.toprc에 설정된 내용 저장|
|q|op 종료|


*top 보기 수정 단축키(출력되는 메인 정보 창 중 상단의 정보 수정)*


|명령어|설명|
|------|---|
|S|umulative 모드 선택/해제|
|i|idle 프로세스 정보 출력/해제|
|I|Irix나 솔라리스 정보 출력/해제|
|c|명령행에서 실행한 명령어 자체로 출력/해제|
|l|로드 평균 정보 출력/해제|
|m|메모리 정보 출력/해제|
|t|요약된 정보만 출력/해제|


*top 정렬 단축키(메인 창에서 실행하는 명령으로 현재 정보를 사용자의 요구대로 정렬)*


|명령어|설명|
|------|---|
|r|프로세스 우선순위 변경|
|N|pid 정보 기준으로 정렬|
|A|age 정보 기준으로 정렬|
|P|CPU 사용량 기준으로 정렬|
|M|적재된 메모리 사용량 기준으로 정렬|
|T|시간/누적시간 기준으로 정렬|
|u|지정한 사용자 정보만 출력|


*top 사용 예시*


![topexample01](https://user-images.githubusercontent.com/96333096/171324519-52a13174-1320-4f43-90d2-c4945d1809f1.png)



**2) 유닉스 리눅스 명령어(ps)**
- 프로세스의 현재 상태 출력


***ps [옵션]***


(1) 전체 프로세스와 관련된 옵션


- -A : 모든 프로세스 출력
- -N : -A 옵션에서 ps 프로세스를 제외하고 출력
- -a : 세션 리더와 터미널에 속하지 않는 프로세스를 제외하고 출력
- -d : 세션 리더를 제외한 프로세스 출력
- -e : 커널 프로세스를 제외한 프로세스 출력
- T : 현재 터미널의 모든 프로세스 출력
- a : 현재 터미널의 사용자 고유 프로세스 출력
- r : 현재 실행 중인 프로세스 출력
- x : 터미널이 없는 프로세스 출력


(2) 특정 프로세스를 선택하여 보여주는 옵션


- -C : 지정한 명령어 이름과 관련된 정보 출력
- -G : 그룹 ID에 관한 정보 출력
- -U : 사용자 ID에 관한 정보 출력
- -g : 지정한 세션 리더나 그룹명에 관한 정보 출력
- -p : 프로세스 ID 출력
- -s : 세션에 속한 프로세스 지정
- -t : tty 지정
- t : tty 지정
- -u : 사용자 ID 지정
- U : 지정한 사용자 프로세스 출력
- p : 프로세스 ID 지정
- --Group : 실제 그룹이름 또는 ID 지정
- --group : 유효 사용자 이름 또는 ID 지정
- --User : 실제 사용자 이름 또는 ID 지정
- --user : 유효 사용자 이름 또는 ID 지정
- --pid : 프로세스 ID 지정
- --sid : 세션 ID 지정
- --tty : 터미널 지정
- -123 = --sid 123
- 123 = --pid 123


(3) 출력 결과 필드를 제어하는 옵션


- -0 : PID, TTY, STAT, TIME, COMMAND 등 필드 목록 출력
- -c : PID, CLS, PRI, TTY, TIME. CMD 등 필드 목록 출력
- -f : UID, PID, PPID, C, STIME, TTY, TIME, CMD 등 필드를 CMD 필드의 전체 명령어 형태로 출력
- -j : PID, PGID, SID, TTY, TIME, CMD 등 필드 목록 출력
- -l : F, S, UID, PID, PPID, C, PRI, NI, ADDR, SZ, WCHAN, TTY, TIME, CMD 필드의 상세 정보 출력
- -o : 사용자가 정의한 포맷 지정
- -y : -l 또는 l 옵션과 함께 ADDR 필드를 RSS 필드로 출력
- 0 : PID, TTY, STAT, IME COMMAND 필드 정보 출력
- X : PID, STACKP, ESP, EIP, TMOUT, ALARM, STAT, TTY, TIME, COMMAND 필드의 정보를 리눅스 i386 레지스터 형식으로 출력한다.
- j : PPID, PID, PGID, SID, TTY, TPGID, STAT, UID, TIME, COMMAND 필드의 정보를 작업 제어에 관련된 형식으로 출력한다.
- l : F, S, UID, PID, PPID, C, PRI, NI, ADDR, SZ, PSS, WCHAN, TTY, TIME, CMD 필드의 정보를 출력하고 -l 옵션과 함께 PSS 필드를 추가하여 출력한다.
- o : 사용자 지정 형식으로 출력한다.
- s : UID, PID, PENDING, BLOCKED, IGNORED, CAUGHT, STAT, TTY, TIME, COMMAND 필드의 정보를 출력한다.
- u : USER, PID, %CPU, %MEM, VSZ, RSS, TTY, STAT, START, TIME, COMMAND 필드의 정보를 출력한다.
- v : PID, TTY, STAT, TIME, MAJFL, TRS, DRS, RSS, %MEM, COMMAND 필드의 정보를 출력한다.
- --format : 사용자 지정 형식으로 출력한다.


(4) 출력 필드의 내용을 변경하는 옵션


- -H : 프로세스를 계층형으로 출력
- -m : 스레드 정보 출력
- -n namelist : 시스템 이름 리스트 파일 지정
- -w : 너비에 맞게 잘려진 내용을 제한이 없는 너비의 내용으로 출력
- --cols : 스크린 너비 설정
- --columns : 스크린 너비 설정
- --cumulative : 죽은 자식 프로세스 데이터 포함하여 출력
- --forest : 아스키 문자의 프로세스 트리 형태로 출력
- --html : HTML 이스케이프 출력
- --headers : 헤더 라인 반복
- --no-headers : 헤더 안보이게 설정
- --lines : 스크린 높이 설정
- --rows : 스크린 높이 설정
- --sort : 정렬 방식 지정


|필드명|설명|
|------|---|
|ADDR|프로세스 스택 세그먼트 번호|
|BND|커널 스레드가 바인드되는 논리 프로세스 번호|
|C|프로세스 사용량|
|CMD|사용자가 실행한 명령 이름|
|F|프로세스와 스레드 관련 항목|
|SIZE|가상 이미지 크기|
|RSS|프로세스 실제 메모리 크기(KB단위)|
|PID|프로세스 ID|
|PRI|프로세스 스케줄링 우선순위|
|S|프로세스와 커널 스레드 상태|
|LIM|메모리에 대한 소프트 한계 항목|
|NI|프로세스 우선순위 값|
|TIME|프로세스 소비 총 시간|
|UID|사용자 ID|
|WCHAN|프로세스에 거주하는 커널 함수|
|%CPU|마지막 1분동안 프로세스가 사용한 CPU 점유율|
|%MEM|마지막 1분동안 프로세스가 사용한 메모리 점유율|


*ps 사용 예시*



![ps example01](https://user-images.githubusercontent.com/96333096/171322322-809abc61-15da-4f0c-b31f-72bc1dc1f1e2.png)


![ps example02](https://user-images.githubusercontent.com/96333096/171322284-3e909d8d-2c42-4f86-872b-fb9b7f36f509.png)


**3) 유닉스 리눅스 명령어(jobs)**
- 백그라운드로 진행 중인 작업 상태, 작업이 중지된 상태, 변경되었으나 보고되지 않은 상태 등을 표시
- 현재 세션의 작업 상태 확인 및 출력


|상태|설명|
|------|---|
|Running|작업이 일시 중단&종료되지 않고 계속 진행 중|
|Done|작업이 완료되어 0 반환&종료|
|Done (code)|작업이 정상적으로 완료&0이 아닌 코드 반환|
|Stopped|작업 일시 중단|
|Stopped(SIGTSTP)|SIGTSTP 신호가 작업을 일시 중단|
|Stopped(SIGSTOP)|SIGSTOP 신호가 일시 중단|
|Stopped(SIGSTTIN)|SIGTTIN 신호가 작업을 일시 중단|
|Stopped(SIGTTOU)|SIGTTOU 신호가 작업을 일시 중단|


*jobs 사용 예시*


![jobsexample](https://user-images.githubusercontent.com/96333096/171323683-3a9c4f54-26fe-4cb2-b0a6-ec11b4c17bb0.png)


![jobsexample01](https://user-images.githubusercontent.com/96333096/171323705-2a62d177-ca42-4ab6-b0be-3d50f81ee89c.png)


**4) 유닉스 리눅스 명령어(kill)**
- 프로세스에 종료 시그널을 보냄
- 시스템에 예기치 못한 문제가 생긴 프로세스 종료 가능
- kill 명령으로 종료되지 않은 프로세스는 -9 옵션으로 강제 종료


|Root|USER|프로세스 사용자|
|------|---|---|
|2518|PID|프로세스 ID|
|0.1|%MEM|마지막 1분 동안 프로세스가 사용한 메모리의 점유율|
|0.0|%CPU|마지막 1분동안 프로세스가 사용한 CPU 점유율|
|7084|VSZ|가상메모리에 있는 프로세스의 KB 단위 크기|
|1076|RSS|프로세스의 실제 메모리의 크기로 KB 단위|
|?|TTY|연결되어 있는 터미널|
|0:00|TIME|프로세스가 소비한 총 시간|
|Jun07|START|프로세스가 시작된 날짜|
|Ss|STAT|실행되고 있는 프로세스 상태|
|/usr/sbin/sshd|COMMAND|사용자가 실행한 명령 이름|



**5) vim 에디터에서 매크로 활용 방법(q,@)**
- 특정한 움직임 또는 키에 입력을 저장함으로써 반복되는 동작을 쉽고 빠르게 해줌
- q + 알파벳을 통해 매크로 저장 가능


1. 커맨드 모드(esc) 준비
2. q + a-z (a-z사이 키에 recording 시작)
3. 내가 원하는 동작 반복
4. 커맨드 모드(esc)로 돌아온 후 q (recording 종료)
5. 매크로 실행하려면 커맨드 모드에서 @+a-z 


ex) @a (1회 실행) / @@ (방금 실행한 매크로 실행) / 10@a (10회 실행)
