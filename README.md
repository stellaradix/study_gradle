# 1. Build Script Basic

### 1.. hello world

- gradle 의 기본 기능 : task 실행
- $ gradle \<task> : task 실행 명령어
- 옵션 -q : block gradle log
  - $ gradle -q \<task>
  - $ gradle \<task> -q

### 2.. multi tasks

- 여러 개의 task 설정
- 여러 개의 task 실행
  - $ gradle \<task 1> \<task 2> ~
  - $ gradle \<task 1>, \<task 2>, ~

### 3.. task flexible registration

- 유연한 task 등록
- 반복문 코딩을 통한 여러 개의 task 등록

### 4.. task dependencies

- dependsOn : task 의존 설정: 다른 task 를 의존 (여러 개 가능)
- 의존되는 task 위치는 영향없음
  - case 1 : 의존 설정 전에 의존되는 task 정의
  - case 2 : 의존 설정 후에 의존되는 task 정의

### 5.. task manipulation

- tasks.named(\<task>) : 태스크 이름으로 task 지정
- doFirst : 작업목록 시작에 작업 추가
- doLast : 작업목록 끝에 작업 추가

### 6.. task coding

- 빌드 스크립트에서 코딩
- 변수 선언
- 문자열 포맷팅, 문자열 변환
- 반복문

### 7.. default tasks

- defaultTasks : default task 지정 (여러 개 가능)
- $ gradle : default task 모두 실행

### 8.. external dependencies

- 빌드 스크립트에서 외부 라이브러리 필요하는 경우
- buildscript > dependencies > classpath 등록

### 9.. build lifecycle

- 1 Phase : Initialization
- 2 Phase : Configuration
- 3 Phase : Execution