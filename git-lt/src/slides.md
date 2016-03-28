class: center, middle, hero, chapter-1

## <nobr>Gitで安価にLTを作る<br>Git超初心者向け勉強会</nobr>

---
class: normal, chapter-1
# 自己紹介
.card[
15FR 谷部 航太郎  
Twitter: [@dll7](https://twitter.com/dll7)  
Facebook: [ky0615](https://www.facebook.com/ky0615)  
Github: [ky0615](https://github.com/ky0615)  

Developer

- Android Application
  - Java8っぽいsomething
  - Kotlin
- Backend
  - Node.js
  - Python
]

---
class: center, middle, hero, chapter-2

## GITとLTの関係性とは？
---

class: faq, chapter-2

### <nobr>折角Gitの勉強会を開催したんだし、<br>LTのスライドも便利にGitで管理したい</nobr>

Gitではバイナリも管理できるため、PowerPointやKeynoteも管理できる

--

- バイナリでは人間に分かる形で差分表示ができない
- バージョン管理をGitでやる利点はほぼ無い

--

#### → テキストベースでスライドを作れれば良い

---
class: center, middle, inverse
#remark
[ri-mahrk]
.footnote[Go directly to [project site](https://github.com/gnab/remark)]
---
class: normal, chapter-3
# What is remark?
.card[

- Markdownのファイルをスライドに変換
- HTMLとして出力される
- そのため、デザインはCSSで修正する
- github.ioを使えば、スライドを簡単に公開可能
]

---
class: normal, chapter-3
# What is remark?
.card[
#### <nobr>→　Markdownで書けるなら、Git本来の機能を<br>最大限使用して作成することができる</nobr>

- 差分表示
- 複数のユーザーで同時に編集やマージ作業を行う
- 簡単に世界にスライドを公開

]

---
class: normal, chapter-3
# Hot to use
.card[
あらかじめNode.jsを入れておく

```
$ npm install -g grunt-cli yo generator-remark
```

]

--
.card[
.large[.center[![shell](/img/1.jpg)]]
]

---
class: normal, chapter-3
# Hot to use
.card[
## File Tree

```ShellScript
 .
├── Gruntfile.js
├── app.js
├── bower.json
├── couchapp.json
├── dist
├── node_modules
            └── 〜
├── package.json
└── src
            ├── css
            │       └── style.css
            ├── js
            │       ├── remark.js
            │       └── remark.language.js
            ├── layout.html
            └── slides.md

```
]


---
class: normal, chapter-3
# Hot to use

.card[
## Building

```
$ grunt server
```
これで自動的にブラウザが開かれスライドが表示される

あとはmarkdownファイルを編集するだけ

```
$ vim ./src/slides.md
```
]

---
name: how
class: normal, chapter-3
# Hot to use

.card[
## Writing

```remark
# Slide 1
This is slide 1

---

# Slide 2
This is slide 2
```

.slides[
  .first[
  ### Slide 1
  This is slide 1
  ]
  .second[
  ### Slide 2
  This is slide 2
  ]
]

- ページの区切りは`---`で行う。Markdown本来の機能である横棒`</hr>`としては機能しないので注意
- あとは基本的にはMarkdownの仕様に準拠しているため、慣れていないのであれば[Markdown website](http://daringfireball.net/projects/markdown/)なんかのプレビューツールなどを使うと良いと思います。
]

---
class: normal, chapter-3
# Hot to use

.card[
## Code Syntax
コードをブロックで囲めば、シンタックスハイライトをかけることもできます。

これは[github-flavored-markdown](http://github.github.com/github-flavored-markdown/) に準拠しているので

.pull-left[

    ```javascript
    function add(a, b)
      return a + b
    end
    ```
]
.pull-right[

    ```ruby
    def add(a, b)
      a + b
    end
    ```
]

もちろんCSSとHTMLで出力されるため、別のCSSを適応すれば他のテーマで表示することもできる

]

---
class: normal, chapter-3
# Hot to use

.card[
## Inline notes

```
Slide 1 content

???

Slide 1 notes

---

```

スライド中にコメントを残すことができる。

__P__ をタイプすると元のブラウザが発表者モードになり、コメントを見ながら発表する事ができ、  
__C__ をタイプすると発表用の画面を出せるので、そちらをスクリーンの画面にぶち込めばOK

]

---
class: normal, chapter-4
# Thank you for listening

.card[


Slideshow created using [remark](http://github.com/gnab/remark).

]
