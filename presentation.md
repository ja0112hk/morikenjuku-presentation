---

theme: "black"
transition: "slide"
slideNumber: false
title: "Webアクセシビリティについて（WAI-ARIAとJS）"

---

##   Webアクセシビリティについて
<span style="color:skyblue">（WAI-ARIAとJS）</span>

---
##### こっぺ<br>
##### 2021-9-18

---

#### 自己紹介
- こっぺ
- 前職（警察、市役所）
- 現職（9/21~Web制作会社勤務）
- もりけん塾（8月~）
- 目標（フロントエンジニアとして活躍、JSでゲーム作る）

---

#### Webアクセシビリティ

---

#### 全てのユーザーが同じ体験を得られるようにすること

---

<div style="width: 200px;color:black;background:white;border-radius:30px;margin:0 auto;box-shadow:0 5px 0 gray;" >見る</div>

<button>見る</button>

---

#### Q.スクリーンリーダーではどのように伝わるか

---

###### １つ目のボタン
```
<div>見る</div>
```
<br>

- ##### あれ、読み上げられない…{.fragment .fade-in-then-semi-out"}
- ##### とゆうか、フォーカスされない…{.fragment .fade-in-then-semi-out"}

---

###### ２つ目のボタン
```
<button>見る</button>
```
<br>

- ##### フォーカスが当たる！{.fragment .fade-in-then-semi-out"}
- ##### 「ボタン、見る」と読み上げられた！{.fragment .fade-in-then-semi-out"}

---

##### 問題点

---

- ##### ブラウザがボタンと認識できない{.fragment .fade-in-then-semi-out"}
- ##### JS、CSSでボタンに見えるものを作れてしまう{.fragment .fade-in-then-semi-out"}
- ##### 結果、全てのユーザーが平等に扱えない…{.fragment .fade-in-then-semi-out"}

---

## WAI-ARIA

---

## WAI-ARIAとJS

---

## 参考文献

---
