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

### 文字サイズ

| クラス名 | 対応するCSS | 見た目のサイズ |
|---|---|---|
| `text-xs` | font-size: 0.75rem | 極小 |
| `text-sm` | font-size: 0.875rem | 小さい |
| `text-base` | font-size: 1rem | 標準 |
| `text-lg` | font-size: 1.125rem | 少し大きい |
| `text-xl` | font-size: 1.25rem | 大きい |
| `text-2xl` | font-size: 1.5rem | より大きい |
| `text-3xl` | font-size: 1.875rem | 見出し向け |
| `text-4xl` | font-size: 2.25rem | 大見出し |
| `text-5xl` | font-size: 3rem | 特大 |

### 文字の太さ・スタイル

| クラス名 | 意味 |
|---|---|
| `font-thin` | 極細 |
| `font-normal` | 通常 |
| `font-medium` | やや太め |
| `font-semibold` | 少し太字 |
| `font-bold` | 太字 |
| `font-extrabold` | 極太 |
| `italic` | 斜体 |
| `underline` | 下線 |
| `line-through` | 打ち消し線 |
| `tracking-wide` | 文字間隔を広げる |
| `leading-relaxed` | 行間を広げる |

### 文字の色

| クラス名 | 意味 |
|---|---|
| `text-white` | 白 |
| `text-black` | 黒 |
| `text-gray-500` | グレー |
| `text-red-500` | 赤 |
| `text-blue-500` | 青 |
| `text-green-500` | 緑 |
| `text-yellow-500` | 黄色 |
| `text-sky-400` | 水色 |
| `text-purple-500` | 紫 |

> 数字は明るさ（100=薄い ～ 900=濃い）を表します

### 背景色

| クラス名 | 意味 |
|---|---|
| `bg-white` | 白背景 |
| `bg-black` | 黒背景 |
| `bg-gray-100` | 薄いグレー背景 |
| `bg-gray-900` | 濃いグレー背景 |
| `bg-blue-500` | 青背景 |
| `bg-blue-800` | 濃い青背景 |
| `bg-red-500` | 赤背景 |
| `bg-green-500` | 緑背景 |
| `bg-transparent` | 透明（背景なし） |

### 枠・角丸・影

| クラス名 | 意味 |
|---|---|
| `border` | 枠線（1px） |
| `border-2` | 枠線（2px） |
| `border-gray-300` | グレーの枠線 |
| `rounded` | 少し角丸 |
| `rounded-lg` | 角丸（大きめ） |
| `rounded-2xl` | 角丸（かなり大きい） |
| `rounded-full` | 完全な丸（円形） |
| `shadow` | 薄い影 |
| `shadow-md` | 中くらいの影 |
| `shadow-lg` | 大きい影 |
| `shadow-xl` | 特大の影 |
| `shadow-none` | 影なし |

### 余白（padding・margin）

> `p`=padding（内側）、`m`=margin（外側）  
> `t`=top、`b`=bottom、`l`=left、`r`=right、`x`=左右、`y`=上下

| クラス名 | 意味 |
|---|---|
| `p-1` | 内側の余白 小（0.25rem） |
| `p-4` | 内側の余白 中（1rem） |
| `p-8` | 内側の余白 大（2rem） |
| `px-4` | 左右の内側余白 |
| `py-2` | 上下の内側余白 |
| `pt-4` | 上の内側余白 |
| `m-4` | 外側の余白 |
| `mt-4` | 上の外側余白 |
| `mb-2` | 下の外側余白 |
| `mx-auto` | 左右中央揃え（横幅固定と組み合わせる） |

### 幅・高さ

| クラス名 | 意味 |
|---|---|
| `w-full` | 横幅100% |
| `w-1/2` | 横幅50% |
| `w-96` | 横幅固定（24rem） |
| `w-auto` | 自動（内容に合わせる） |
| `max-w-xl` | 最大横幅を制限 |
| `max-w-4xl` | 最大横幅（大） |
| `h-full` | 高さ100% |
| `h-screen` | 画面の高さ |
| `min-h-screen` | 最低でも画面の高さ |

### レイアウト（Flexbox）

| クラス名 | 意味 |
|---|---|
| `flex` | 横並びにする |
| `flex-col` | 縦並びにする |
| `flex-wrap` | 折り返しあり |
| `items-center` | 縦方向の中央揃え |
| `items-start` | 縦方向の上揃え |
| `justify-center` | 横方向の中央揃え |
| `justify-between` | 両端揃え |
| `justify-end` | 右揃え |
| `gap-4` | 要素間の隙間（1rem） |
| `gap-8` | 要素間の隙間（2rem） |

### レイアウト（Grid）

| クラス名 | 意味 |
|---|---|
| `grid` | グリッドレイアウト |
| `grid-cols-2` | 2列のグリッド |
| `grid-cols-3` | 3列のグリッド |
| `grid-cols-4` | 4列のグリッド |
| `col-span-2` | 2列分の幅を占める |

### 表示・非表示

| クラス名 | 意味 |
|---|---|
| `hidden` | 非表示（display: none） |
| `block` | ブロック要素として表示 |
| `inline` | インライン要素として表示 |
| `inline-block` | インラインブロック |
| `opacity-50` | 半透明（50%） |
| `opacity-0` | 完全透明 |
| `overflow-hidden` | はみ出し部分を隠す |

### カーソル・操作

| クラス名 | 意味 |
|---|---|
| `cursor-pointer` | カーソルを手の形にする |
| `select-none` | テキスト選択を無効にする |
| `pointer-events-none` | クリックを無効にする |

### ホバー・フォーカス（インタラクション）

| クラス名 | 意味 |
|---|---|
| `hover:bg-blue-600` | マウスを乗せたとき背景色変更 |
| `hover:text-white` | マウスを乗せたとき文字色変更 |
| `hover:shadow-xl` | マウスを乗せたとき影を強調 |
| `focus:outline-none` | フォーカス時の枠線を消す |
| `transition` | 変化をなめらかにする |
| `duration-300` | アニメーション時間（300ms） |

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
