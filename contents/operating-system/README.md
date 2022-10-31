Operating System (운영체제)
==========
## 프로세스
* 프로그램  
  보조 기억장치(SSD)에 존재하며 실행되기를 기다리는 명령어(코드)와 정적인 데이터의 묶음
-> 프로그램은 생명이 존재하지 않음

* 프로세스  
실행 중인 프로그램
프로그램의 명령어와 정적 데이터가 메모리에 적재되면 생명이 생김

> Q.프로세스를 여러개 실행 시킬 수 있을까?

컴퓨터의 세상에서 여러개의 프로세스가 동시에 실행되는 건 놀라운 일!
-> 하나의 CPU 즉, 프로세서는 한 순간에 하나의 프로세스만 실행 가능

> Q. 그럼 어떻게 여러개의 프로세스가 동시에 실행 가능할까?

프로세스가 동시에 여러개가 실행될 수 있는 이유
운영체제가 엄청나게 빠르게 CPU가 실행할 프로세스를 교체하고 있기 때문
사실은 여러개의 프로세스가 실행되고 있는 것이 아니라
눈 깜박할 사이에 이 교체가 여러번 일어나기 때문에 여러개의 프로세스가 
실행되고 있다고 느끼는 것 뿐임!

### 프로세스의 구성
> 프로세스에 대한 정보는 프로세스 제어블록(PCB, Process Control Block)또는 
프로세스 기술자(process descriptor)라고 부르는 자료구조에 저장됨
대부분 PCB라고 부름
이 자료구조는 크게 다음 같은 정보를 담고 있다

* PID (Process IDentification)  
```
운영체제가 각 프로세스를 식별하기 위해 부여된 프로세스 식별번호
```

* 프로세스 상태
```
CPU는 프로세스를 빠르게 교체하면서 실행하기 때문에  
실행 중인 프로세스도 있고 대기 중인 프로세스도 있음  
이런 프로세스 상태 말하고 이 정보를 저장하고 있음
```

* 프로그램 카운터
```
CPU가 다음으로 실행할 명령어를 가리키는 값  
CPU는 기계어를 한 단위씩 읽어서 처리  
프로세스를 실행하기 위해 다음으로 실행할 기계어가 
저장된 메모리 주소를 가리키는 값
```

* 스케줄링 우선순위