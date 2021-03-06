# Index
## 목적
- 테이블 컬럼 색인화, 책의 목차 기능
- 데이터 정렬 후 별도의 메모리 공간에 저장
    - 컬럼 값(key), 물리 주소(value)

## 장점
1. 정렬된 형태의 데이터를 가짐
    - 테이블 검색 속도, 성능 향상

## 단점
1. 잦은 데이터 수정 시 성능 저하
    - 데이터 수정 시 인덱스도 수정
    - 데이터 제거 시 인덱스는 제거되지 않음
        - '사용하지 않음' 처리 후 남겨둠
        - 실제 데이터에 비해 인덱스 과도하게 커지는 문제점
    
2. 잘못 사용 시 검색 성능 저하
    - 나이, 성별과 같은 값의 범위가 좁은 경우
        - 인덱스 확인 후 다시 많은 데이터 조회
        - 비효율적

## 사용하면 좋은 경우
- 수정이 자주 발생하지 않는 컬럼
- 조회가 잦은 컬럼
- 데이터의 중복도가 낮은 컬럼

## 인덱스 자료구조
### 해시테이블
- key, value = 컬럼의 값, 데이터 위치
- 등호 연산에만 최적화
- 부등호 연산에 취약하므로 잘 사용되지 않음

### B+Tree
<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FbAARBC%2FbtrdDydoUp7%2F9h4KOXBRyDNKpKDAe2ugq0%2Fimg.png">

- 오직 leaf node에만 데이터를 저장
    - leaf node가 아닌 node에서는 자식 포인터만 저장
    - 특정 key 접근 위해 leaf node까지 가야함

- leaf node끼리는 Linked list로 연결.
    - 효율적인 순차 검색, 부등호 연산 가능


