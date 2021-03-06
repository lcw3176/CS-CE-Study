# DFS (깊이 우선 탐색)
## 개요, 특징
- 루트 노드 or 임의의 시작 노드에서 다음 분기(branch)로 가기 전에 해당 가지를 끝까지 탐색
- 시작 정점 -> 가까운 정점(a) -> 이웃 노드 전부 방문(b) -> 정점 복귀(a) -> 다른 이웃 노드 방문(c) -> 반복 후 완료
- 구현 방법
    - 재귀
    - 반복문
    - 스택
- 시간 복잡도
    - 인접 행렬: O(V^2) 
    - 인접 리스트: O(V + E) 
- 용어 정리
    - V(Vertex): 노드, 정점 
    - E(edge): 노드 간 연결선, 간선 
    - arc: 방향성 엣지
<div>
    <img src="https://user-images.githubusercontent.com/59993347/135012975-a3caf234-f263-4211-8628-0bc962471546.png">
    <p>출처 https://www.geeksforgeeks.org/graph-data-structure-and-algorithms/</p>
</div>


## 대표적인 문제들
- 특정 경로
- 모든 경우의 수
