# 오탈자 및 개선사항

## 16.2.10 (pg. 426)

페이지 하단 설명에 오타가 있습니다.

17.1 절이 아니라 16.1 절로 돌아가야합니다.

```diff
- 모두 제대로 작동한다면 17.1절로 돌아가서 다시 한번 개념을 훑어 보세요. 그리고 다음 내용을 계속 진행해주세요.
+ 모두 제대로 작동한다면 16.1절로 돌아가서 다시 한번 개념을 훑어 보세요. 그리고 다음 내용을 계속 진행해주세요.
```

## 18.3.1.5 (pg.500)

페이지 상단 `connect` 함수의 `loadingPost` 와 `loadingUsers` 부분에 오탈자가 있습니다.

```diff
export default connect(
  ({ sample, loading }) => ({
    post: sample.post,
    users: sample.users,
-    loadingPost: loading.GET_POST,
-    loadingUsers: loading.GET_USERS
+    loadingPost: loading['sample/GET_POST'],
+    loadingUsers: loading['sample/GET_USERS']
  }),
  {
    getPost,
    getUsers
  }
)(SampleContainer);
```

## 20.3.5 (pg. 560)

chunks.js 로 끝나는 키를 찾아서 스크립트 태그로 변환하는 부분에 오탈자가 있습니다.

`manifest[key]` 가 아닌 `manifest.files[key]` 로 바꿔주어야 합니다.

```diff
const chunks = Object.keys(manifest.files)
  .filter(key => /chunk\.js$/.exec(key)) // chunks.js 로 끝나는 키를 찾아서
-  .map(key => `<script src="${manifest[key]}"></script>) // 스크립트 태그로 변환하고
+  .map(key => `<script src="${manifest.files[key]}"></script>) // 스크립트 태그로 변환하고
  .join(''); // 합침
```

## 23.4.2 (pg. 697)

user.js 파일의 경로에 오타가 있습니다. `modles` 디렉터리가 아닌 `models` 디렉터리입니다.

```
- src/modles/user.js - generateToken
+ src/models/user.js - generateToken
```