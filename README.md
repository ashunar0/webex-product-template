# アプリの名前

## 動かし方

```bash
npm install
npm run dev
```

## 担当

| ページ | 担当 | ファイル |
| --- | --- | --- |
| ログイン | | `src/pages/login/` |
| ホーム | | `src/pages/home/` |

## データの形

| コレクション | フィールド |
| --- | --- |
| | |

## AI に最初に貼る文

ChatGPT などにコードを書いてもらうときは、会話の最初にこの文を貼ってください。

```markdown
これから React でアプリを作ります。コードを書くときは、次の前提を必ず守ってください。

## 使っているもの
- Vite + React 19。JavaScript で書く（TypeScript は使わない）
- パッケージの管理は npm
- 画面の切り替えは React Router v7。`react-router` から import する（`react-router-dom` は使わない）。`<BrowserRouter>` と `<Routes>` / `<Route>` で書く
- データは Firebase v13 の Firestore。`firebase/firestore` から関数を import して書く（`firebase.firestore()` のような古い書き方はしない）
- ログインは Firebase Authentication の Google ログインだけ
- 見た目は素の CSS。Tailwind や UI ライブラリは使わない

## ファイルの置き場所
- Firebase の設定は `src/firebase.js` にあり、`db` と `auth` を export している。新しく `initializeApp` しない
- ページは `src/pages/home/HomePage.jsx` のように、ページごとのディレクトリに置く。CSS は同じ場所に `HomePage.css`
- そのページでしか使わない部品は、同じディレクトリに置く。複数のページで使う部品は `src/components/`
- ログイン中のユーザーは、`App.jsx` から props の `user` で受け取る。ページの中で `onAuthStateChanged` や `auth.currentUser` を使わない

## 書き方
- Firestore の読み書きは、そのページのコンポーネントの中に直接書く。`api.js` や `services/` のように別のファイルに分けない
- 使うのは `useState`・`useEffect`・props だけ。カスタムフック・Context・状態管理ライブラリは使わない
- 関数はアロー関数で書く（コンポーネントだけ `function`）
- 取ってくる関数（例：`getPosts`）と送る関数（例：`addPost`）は分ける。送ったあとは `getPosts()` で取り直す

## データの形
（上の「データの形」の表をここに貼る）

## 答え方
- 上にない書き方を使うときは、必ず説明した上で使ってください
- どのファイルのどこに書くのかを示してください
```
