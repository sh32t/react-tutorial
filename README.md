# React.jsのチュートリアル
## プロジェクトの作成
```ps1
npm init -y
```
## Reactのインストール
```ps1
npm install react
npm install react-dom
```
## コンパイラのインストール
```ps1
npm install browserify
npm install reactify
```
## JSXファイルの作成
#### `sample.html`を作成する。
```html
<body>
    <div id="root"></div>
    <script src="sample.js"></script>
</body>
```
#### `sample.jsx`を作成する。
```jsx
const React = require('react');
const ReactDOM = require('react-dom');

ReactDOM.render(
    <h1>Hello, world!</h1>,
    document.getElementById('root')
);
```

## JSXからJavaScriptへの変換
```ps1
.\node_modules\.bin\browserify -t reactify sample.jsx -o sample.js
```

### 参考
#### [React16 最小構成のビルド環境 browserify reactify JSXあり](https://qiita.com/standard-software/items/781ec3f491f4f1bea7b6)