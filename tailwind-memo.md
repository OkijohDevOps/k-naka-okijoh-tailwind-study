# Tailwind CSS まとめ

## そもそも CSS とは？

CSS（Cascading Style Sheets）は、HTMLで作った文字や要素に  
**「色・大きさ・余白・レイアウト」** などの見た目を付けるための言語です。  
CSSがないと、すべてのページが飾り気のない黒文字だけになります。

```css
/* 素のCSS の例 */
h1 {
  font-size: 2rem;   /* 文字サイズ */
  color: #991b1b;    /* 文字色 */
}
```

---

## Tailwind CSS とは？

Tailwind CSS は **「ユーティリティファースト」** という考え方の CSS フレームワークです。  
「背景を青に」「文字を大きく」「余白をつける」といった  
**小さなクラスを HTML に直接組み合わせる** だけでデザインができます。

```html
<!-- Tailwind CSS の例 -->
<h1 class="text-3xl font-bold text-red-800">名嘉 健太</h1>
```

| クラス名 | 対応するCSS |
|---|---|
| `text-3xl` | font-size: 1.875rem |
| `font-bold` | font-weight: bold |
| `text-red-800` | color: #991b1b |

---

## どうやって使う？

最も簡単な方法は **CDN（ネット経由）** で読み込むことです。  
以下の1行を `<head>` に書くだけで Tailwind の全クラスが使えます。

```html
<script src="https://cdn.tailwindcss.com"></script>
```

---

## よく使うクラス一覧

### 文字

| クラス名 | 意味 |
|---|---|
| `text-sm` | 小さい文字 |
| `text-3xl` | 大きい文字 |
| `font-bold` | 太字 |
| `text-red-500` | 赤い文字 |

### 背景・枠

| クラス名 | 意味 |
|---|---|
| `bg-blue-800` | 青い背景 |
| `rounded-2xl` | 角丸 |
| `shadow-lg` | 影 |
| `border` | 枠線 |

### 余白

| クラス名 | 意味 |
|---|---|
| `p-8` | 内側の余白（padding） |
| `mt-4` | 上の外側余白（margin-top） |
| `mb-2` | 下の外側余白（margin-bottom） |
| `gap-4` | 要素間の隙間 |

### レイアウト

| クラス名 | 意味 |
|---|---|
| `flex` | 横並びにする |
| `justify-center` | 中央揃え |
| `w-96` | 横幅を固定 |
| `min-h-screen` | 画面の高さ以上 |

---

## Tailwind CSS vs 素のCSS 比較

| 項目 | Tailwind CSS | 素のCSS |
|---|---|---|
| 書き方 | HTMLの `class` に直接書く | `<style>` や別ファイルに書く |
| スタイルの場所 | HTMLとスタイルが一体 | HTMLとCSSが分離 |
| クラス名の例 | `bg-blue-800` `text-3xl` `p-8` | `.card` `.role` `.info` |
| CSSファイルは必要？ | 不要（CDN1行でOK） | 必要（自分で書く） |
| カスタマイズ | クラスを組み合わせるだけ | CSSを直接編集 |
| 学習コスト | Tailwind独自のクラス名を覚える | 標準CSSの知識だけでOK |
| 向いている場面 | 素早くUIを作りたいとき | 細かく作り込みたいとき |

---

## 参考ファイル

- `meishi.html` … Tailwind CSS と素のCSSで作った名刺カード比較ページ
