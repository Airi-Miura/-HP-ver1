# Snowboard Coaching LP

スノーボードコーチングサービス用のランディングページです。HTML、CSS、JavaScriptのみで作成しているため、`index.html` をダブルクリックするだけで表示できます。

## ファイル構成

```text
snowboard-coaching-lp/
├── index.html
├── style.css
├── script.js
├── README.md
├── robots.txt
├── sitemap.xml
├── favicon.svg
└── assets/
    ├── icons/
    └── images/
```

## 編集方法

### 文章を変更する

`index.html` をテキストエディタで開き、見出しや本文を変更してください。

よく編集する場所は以下です。

- Heroのキャッチコピー: `あなたの滑りを、一つずつ言語化する。`
- CTAボタン: `無料相談はこちら`
- 料金: `体験`、`通常`、`動画解析付き`
- FAQ: `<details>` タグの中
- 最後の問い合わせ導線: `id="contact"` のセクション

### 料金を変更する

`index.html` の `id="price"` セクション内にある以下のような行を変更します。

```html
<p class="price">¥22,000<span>/ 半日</span></p>
```

金額、時間、プラン名、内容は自由に書き換えられます。

### 色を変更する

`style.css` の一番上にある `:root` を編集します。

```css
:root {
  --accent: #6ec6ff;
  --ice: #d9f3ff;
  --blue: #2b6cb0;
}
```

サイト全体のアクセントカラーをまとめて変更できます。

## 問い合わせ先変更方法

`index.html` の `id="contact"` セクションにあるリンクを変更してください。

```html
<a class="button primary" href="https://mail.google.com/mail/?view=cm&fs=1&to=snow.lesson.contact@gmail.com">問い合わせボタン</a>
<a class="button secondary" href="https://docs.google.com/forms/d/e/1FAIpQLScOuVmrlRJT56gElZe1HvV9EYCYRquhjfrBi6x8B--QABFhRg/viewform?usp=dialog" target="_blank" rel="noopener">Googleフォーム</a>
```

変更例:

- Gmail宛先: `snow.lesson.contact@gmail.com`
- Googleフォーム: 作成したフォームの共有URL

## SEO設定の変更

公開前に `https://example.com/` を実際のURLに置き換えてください。

対象ファイル:

- `index.html` の `canonical`
- `index.html` の `og:url`
- `index.html` の JSON-LD内 `url`
- `robots.txt` の `Sitemap`
- `sitemap.xml` の `loc`

ページタイトルと説明文は `index.html` の上部で編集できます。

```html
<title>スノーボード コーチング | 滑りを言語化するマンツーマンレッスン</title>
<meta name="description" content="...">
```

## 公開方法

### 通常のサーバーにアップロードする場合

1. `snowboard-coaching-lp` フォルダの中身をすべてアップロードします。
2. サーバー上で `index.html` がトップページになるように配置します。
3. 公開URLに合わせて `canonical`、OGP、`robots.txt`、`sitemap.xml` を更新します。

## Netlifyへのアップロード方法

1. Netlifyにログインします。
2. 管理画面で「Add new site」を選びます。
3. 「Deploy manually」を選びます。
4. `snowboard-coaching-lp` フォルダをドラッグ＆ドロップします。
5. 公開後に表示されるURLを確認します。
6. 独自ドメインを使う場合は、Netlifyの「Domain settings」から設定します。
7. 公開URLが決まったら、`index.html`、`robots.txt`、`sitemap.xml` の `https://example.com/` を実際のURLに変更して再アップロードします。

## Lighthouse対策

このLPでは以下を実装しています。

- セマンティックHTML
- title、meta description、canonical
- OGP
- favicon
- robots.txt
- sitemap.xml
- JSON-LD構造化データ
- FAQ構造化データ
- Breadcrumb
- CSS中心の軽量デザイン
- 外部ライブラリ不使用
- アクセシビリティ用スキップリンク
- `prefers-reduced-motion` 対応
- JavaScriptは `defer` で読み込み

## 注意点

このテンプレートには実画像を入れていません。将来写真を追加する場合は、画像を `assets/images/` に入れて、HTMLの `img` タグには必ず `loading="lazy"` と適切な `alt` を設定してください。
