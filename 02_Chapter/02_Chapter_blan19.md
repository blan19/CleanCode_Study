## 의미 있는 이름 짓기

간단한 코드를 한번 보겠습니다.

```javascript
const getPosts = async (i) => {
  const p = await fetch(`apiUrl/${i}`, { method: "GET" }).then((r) => r.json());
};
```

한 번에 보면 i가 뭘 뜻하고, p가 뭘 뜻하는지 모르겠습니다.

함수의 네임을 보고 나중에야 p가 포스트고 i가 ID인 걸 유추할순 있겠죠.

하지만 다음 코드를 보겠습니다.

```javascript
const getPostForId = async (postId) => {
  const post = await fetch(`apiUrl/${postId}`, { method: "GET" }).then((r) =>
    r.json()
  );
};
```

좀 더 의미가 명확해졌습니다.

첫번째 코드보단 한 눈에 무엇을 뜻하는지 확인이 가능합니다.
