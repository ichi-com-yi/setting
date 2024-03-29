## ディレクトリ
- `.vscode` vscodeの設定ファイルなどが収められたディレクトリ
  - `csscomb.json` csscombの設定ファイル
  - `settings.json` vscodeの設定ファイル
- `assets` 画像、css、sassファイルが収められたディレクトリ
  - `images` 画像が収められたディレクトリ
  - `css` cssが収められたディレクトリ
   - `style.css` コンパイルされたcss
   - `style.css.map` コンパイルされたcssのmapファイル
  - `sass` sassが収められたディレクトリ
    - `base` 基本となる設定やリセット用
    - `core` 変数、関数やmixin用
    - `elements` パーツ用
    - `module` ブロック単位用
    - `utility` 補助用
    - `style.scss` インポート用
- `.editorconfig` EditorConfigの設定ファイル
- `.gitignore` gitの除外ファイル
- `prepros.config` preprosの設定ファイル
- `README.md` 説明などを記載

-- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --

## 使用する環境など
非`node.js`環境です。`prepros`やvscodeの拡張機能である`liveSassCompiler`などでサクッとコンパイルして`csscomb`で整形する環境を想定しています。

## 注意点
`prepros`のみ`dart-sass`に対応しています。`csscomb`のフォーマットは`dart-sass`ですとエラーがでます。`liveSassCompiler`は`dart-sass`には非対応です。

## フォーマットの実行
VSCodeのコマンドパレットより`csscomb`を実行。
```
コマンドパレットは『F1』キー、またはショートカットキー『Win：Ctrl + Shift + P』『Mac：Cmd + Shift + P』
```

## csscombルール
| 説明 |     |
| --- | --- |
| セミコロンの設定（true or false）| "always-semicolon": true, |
| インデントのサイズ設定（なし：""、半角スペース2個："  "、タブ："\t" ）| "block-indent": "  ", |
| 色コードの設定（lower or camel）| "color-case": "lower", |
| 色コードのショートハンド（true or false）| "color-shorthand": true, |
| 要素の指定（lower or camel）| "color-case": "lower", |
| EOFでの改行（true or false）| "element-case": "lower",, |
| 小数点数値の0.を省略するか（true or false））| "leading-zero": false, |
| クォートの設定（single　or double）| "quotes": "single", |
| 「：」の後に入れる文字を設定 | "space-after-colon": " ", |
| 「>」や「+」の後に入れる文字を設定| "space-after-combinator": " ", |
| 「{」のあとに入れる文字を設定 | "space-after-opening-brace": "\n  ", |
| 複数要素指定時「,」の後に入れる文字を設定 | "space-after-selector-delimiter": "\n", |
| 「：」の前に入れる文字を設定 | "space-before-colon": "", |
| 「>」や「+」の前に入れる文字を設定 | "color-case": "space-before-closing-brace": "\n", |
| 「}」の前に入れる文字を設定 | "space-before-combinator": " ", |
| 「{」の前に入れる文字を設定 | "space-before-opening-brace": " ", |
| 複数要素指定時「,」の前に入れる文字を設定 | "space-before-selector-delimiter": "", |
| 末尾のスペースを削除するか（true or false）| "strip-spaces": true, |
| 値が0の場合に単位を省略するか（true or false）| "unitless-zero": true, |
| ベンダープレフィックスを整列するか（true or false）| "vendor-prefix-align": true, |
| 空のルールセットを残すか（true or false）| "remove-empty-rulesets": true, |

## 追加
ブランチ`dev1`追加。
各ファイルにコメントアウトでちょっとした説明を追加。

### 2022-03-11
ブランチ`dev2`追加
`utilities``mixin``variables`を追加
### 2022-03-14
ブランチ`dev3`追加
`mixin`にメディアクエリを追加。
`variables`にブレイクポイント用の変数を追加。
`function`に関数を追加。
### 2022-03-16
ブランチ`dev4`追加
`function`に関数を追加。
### 2023-06-29
`.vscode`以下`csscomb.json`と`settings.json`最新版に  
`.gitignore`と`.editorconfig`最新版に
`.prettierignore`と`.prettierrc`追加
