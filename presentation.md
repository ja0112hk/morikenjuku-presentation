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

#### <div style="text-align:left;">全てのユーザーが同じ体験を得られるようにすること</div>

---

<div style="width: 200px;color:black;background:white;border-radius:30px;margin:0 auto;box-shadow:0 5px 0 gray;" >見る</div>

<button>見る</button>

---

どちらが押せそう？

---

#### Q.スクリーンリーダーではどのように伝わるか

---

##### １つ目のボタン
```
<div>見る</div>
```
<br>

##### あれ、読み上げられない…{.fragment .fade-in-then-semi-out"}
##### とゆうか、フォーカスされない…{.fragment .fade-in-then-semi-out"}

---

##### ２つ目のボタン
```
<button>見る</button>
```
<br>

##### フォーカスが当たる！{.fragment .fade-in-then-semi-out"}
##### 「ボタン、見る」と読み上げられた！{.fragment .fade-in-then-semi-out"}

---

##### 問題点

---

- ##### ブラウザがボタンと認識できない{.fragment .fade-in-then-semi-out"}
- ##### JS、CSSでボタンに見えるものを作れてしまう{.fragment .fade-in-then-semi-out"}
- ##### 結果、全てのユーザーが平等に扱えない…{.fragment .fade-in-then-semi-out"}


---

## WAI-ARIA

---

#### <span style="color:skyblue">WAI-ARIA</span>とは

<div style="text-align:left;"><span style="color:skyblue">W</span>eb <span style="color:skyblue">A</span>ccessibility <span style="color:skyblue">I</span>nitiative (W3C の中で、Web アクセシビリティに関する仕様を検討する部会) が策定した、<span style="color:skyblue">A</span>ccessible  な <span style="color:skyblue">R</span>ich <span style="color:skyblue">I</span>nternet <span style="color:skyblue">A</span>pplications に関する仕様です。</div>

---

```
<ul role="tablist">
    <li role="presentation">
        <a role="tab" aria-controls="panel1" aria-selected="true">tab1</a>
        <a role="tab" aria-controls="panel2" >tab2</a>
        <a role="tab" aria-controls="panel3" >tab3</a>
    </li>
</ul>
<div>...
<div>...
```

---

#### <div style="text-align:left;">HTMLの要素に属性を与えることで、支援技術のユーザー向けに情報を追加したり、変更したりする手段を提供している</div>

---

#### 先程のボタンに実装してみる余談ボタンの属性

---

```
<div role="button" aria-label="見る">見る</div>
```

---

WAI-ARIAの３つの機能
- ロール{.fragment .fade-in-then-semi-out"}
- プロパティ{.fragment .fade-in-then-semi-out"}
- ステート{.fragment .fade-in-then-semi-out"}

---

#### ロール
---
> 役割{.fragment .fade-in-then-semi-out"}
#### RPG風に表現すると…{.fragment .fade-in-then-semi-out"}
> 「職業、種族」剣士、僧侶、魔法使い{.fragment .fade-in-then-semi-out"}
#### 例）`<div>`に`button`ロールで支援技術がボタンと認識{.fragment .fade-in-then-semi-out"}

---

#### プロパティ
---
> 特性、能力{.fragment .fade-in-then-semi-out"}
#### RPG風に表現すると…{.fragment .fade-in-then-semi-out"}
> 剣士→剣を装備できる{.fragment .fade-in-then-semi-out"}
#### 限定されるものもある{.fragment .fade-in-then-semi-out"}
> 魔法は魔法使いしか使えない{.fragment .fade-in-then-semi-out"}
#### 例）`aria-label`「説明のテキスト追加」{.fragment .fade-in-then-semi-out"}
#### 例）`aria-required`「フォームなどでしか使えない」{.fragment .fade-in-then-semi-out"}

---

#### ステート
---
> 状態{.fragment .fade-in-then-semi-out"}
#### RPG風に表現すると…{.fragment .fade-in-then-semi-out"}
> 健康状態、どんな装備を身に着けた、誰が仲間に{.fragment .fade-in-then-semi-out"}
#### 例）`aria-hidden`「目に見える？見えない？」{.fragment .fade-in-then-semi-out"}

---

#### 注意すべきポイント
- 暗黙のロールで目的を果たせる場合はそれを使う
- 必要な場合以外ネイティブのセマンティクスを変更しない
- すべてキーボードで使用できるよう


---

#### `<button> //暗黙のロール button`
#### `<a> // 暗黙のロール link`

---

```
<h1 role="button">
```

##### `<h1>にbuttonロール…見出しとしての機能を失う`
```
<h1><button></button></h1>
```


---

---

## WAI-ARIAとJS

---

## 参考文献

---
