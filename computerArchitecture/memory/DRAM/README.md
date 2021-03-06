# Memory
## DRAM (Dynamic Random Access Memory)
### Hardware
#### 내부 회로
<img src="https://user-images.githubusercontent.com/59993347/135577191-12e6d8c4-0f69-4b6f-add7-6a0f24214df1.png" width=300>

#### 특징
- 커패시터를 저장소자로 사용
- 전하 누수, 지속적 refresh 필요
- 가격 저렴, 속도 느림
- 메인 메모리에 사용

#### 세부 동작
- Address Line (Word Line)
    - 트랜지스터 on, off
    - 접근 여부 결정
- bit line
    - 데이터 읽기
        1. Address Line on, bit line에는 Vdd / 2 전압 인가
        2. bit line과 커패시터 전하 공유
        3. bit line의 전압 상승, 하강 폭 감지
        4. 상승 시 1, 하강 시 0
    - 데이터 쓰기
        1. Address Line on, 회로 도통
        2. bit line에 전압 인가
        3. 커패시터 충전 or 방전
        4. Address Line off, 데이터 상태 저장 

#### 주소 선택
<img src="https://user-images.githubusercontent.com/59993347/135577181-6c0e9cc4-ac2c-4104-ba71-f0ac75f29bbc.jpg" width=300>

- 8 x 8, 64비트 RAM
    1. 3개의 주소 입력
    2. 디코더를 통해 8개의 주소 생성 가능
    3. 8비트의 저장 공간, 8비트 데이터 출력

<img src="https://user-images.githubusercontent.com/59993347/135578878-4f80c49e-2090-4fed-a549-f0ff9ac1490d.jpg" width=300>

- 64 x 1, 64 비트 RAM
    1. 행 주소선 3개, 열 주소선 3개 필요
    2. 1비트의 저장 공간, 1비트 데이터 출력