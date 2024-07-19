# concat

::: info
이 함수는 [lodash와 완전히 호환](../../../compatibility.md)돼요. `es-toolkit/compat` 라이브러리에서 쓸 수 있어요.
:::

여러 배열과 값을 하나의 배열로 연결해요.

## 인터페이스

```typescript
function concat<T>(...values: Array<T | T[]>): T[]
```

### 파라미터

- `values` (`...(T | T[])`): 연결할 배열이나 값.

### 반환 값

(`T[]`): 모든 배열과 값이 연결된 새 배열.

### 예시

```typescript
// 값을 연결
concat(1, 2, 3); 
// 반환 값: [1, 2, 3]

// 배열을 연결
concat([1, 2], [3, 4]);
// 반환 값: [1, 2, 3, 4]

// 값과 배열을 섞어서 연결
concat(1, [2, 3], 4);
// 반환 값: [1, 2, 3, 4]

// 중첩 배열을 연결하는 경우
concat([1, [2, 3]], 4);
// 반환 값: [1, [2, 3], 4]
```