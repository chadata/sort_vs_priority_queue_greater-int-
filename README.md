`sort`와 `priority_queue`에 사용되는 `greater<int>`는 둘 다 동일한 `std::greater<int>` 비교 함수 객체입니다. 그러나 이들이 각각 작동하는 방식은 다릅니다.

`sort`의 경우, `greater<int>`를 사용하여 원소들을 내림차순으로 정렬하는 데 사용됩니다. 예를 들어:

```cpp
vector<int> v = {3, 1, 4, 1, 5, 9};
sort(v.begin(), v.end(), greater<int>());
// 결과는 {9, 5, 4, 3, 1, 1}이 됩니다.
```

반면 `priority_queue`의 경우, `greater<int>`를 사용하여 최소 우선순위 큐를 구현할 수 있습니다. 기본적으로 `priority_queue`는 최대 우선순위 큐이며 원소는 기본적으로 내림차순으로 저장됩니다. 그러나 `greater<int>`를 사용하여 오름차순으로 원소들을 관리하게 되어 최소 값을 먼저 추출할 수 있습니다.

```cpp
priority_queue<int, vector<int>, greater<int>> pq;
pq.push(3);
pq.push(1);
pq.push(4);
// 여기서 pq.top()은 1을 반환합니다.
```

결론적으로, `greater<int>`는 둘 다 동일한 비교 함수 객체를 사용하지만, `sort`와 `priority_queue`에서 다른 역할을 수행할 수 있습니다. `sort`에서는 내림차순 정렬에 사용되며, `priority_queue`에서는 최소 우선순위 큐를 생성하는 데 사용됩니다.
