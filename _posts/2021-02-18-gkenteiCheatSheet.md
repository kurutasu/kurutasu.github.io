---
layout: post
title:  "【G検定】チートシート"
updated: 2021-02-18
cover:  "/assets/cover_image.jpg"
subheadline:  "G検定まとめ"
categories: 
- AI
---

# はじめに

* [一般社団法人 日本ディープラーニング協会　G検定](https://www.jdla.org/certificate/general/)

* ディープラーニングG検定に向けた情報整理を行う。

* 構成は[シラバス](https://www.jdla.org/certificate/general/#general_No03)に従い、該当項目には「📘」を付す。

* 参考図書

    [ディープラーニング G検定(ジェネラリスト) 公式テキスト](https://www.amazon.co.jp/dp/4798157554)

* 模擬テスト

    [Study-AI G検定 模擬テスト](http://study-ai.com/generalist/)

# １．📘人工知能（AI）とは（人工知能の定義）

## AIの定義

* 専門家の間で共有されている定義はない。

* 人工知能であるかどうかは「人によって違う」。

* 定義の例

    * 「推論、認識、判断など、人間と同じ知的な処理能力を持つ機械（情報処理システム）」
    
    * 「周囲の状況（入力）によって行動（出力）を変えるエージェント（プログラム）」

    * 🎩松尾豊
    
        「人工的につくられた人間のような知能、ないしはそれをつくる技術」

    * 🎩アーサー・サミュエル

        「明示的にプログラムしなくても学習する能力をコンピュータに与える研究分野」

## 人工知能レベル

* レベル1

    シンプルな制御プログラム。**ルールベース**。
 
* レベル2

    古典的な人工知能。**探索・推論**を行う。知識データを利用する。
 
* レベル3

    [**機械学習**](https://d.hatena.ne.jp/keyword/%E6%A9%9F%E6%A2%B0%E5%AD%A6%E7%BF%92)を取り入れた人工知能。多くのデータから入力・出力関係を学習する。
 
* レベル4   

    [**ディープラーニング**](https://d.hatena.ne.jp/keyword/%E3%83%87%E3%82%A3%E3%83%BC%E3%83%97%E3%83%A9%E3%83%BC%E3%83%8B%E3%83%B3%E3%82%B0)を取り入れた人工知能。特徴量による学習を行う。

## AI効果

* [人工知能](https://d.hatena.ne.jp/keyword/%E4%BA%BA%E5%B7%A5%E7%9F%A5%E8%83%BD)の原理がわかると「単純な自動化である」とみなしてしまう人間の心理のこと。

## ロボットとの違い

* [人工知能](https://d.hatena.ne.jp/keyword/%E4%BA%BA%E5%B7%A5%E7%9F%A5%E8%83%BD)では「考える」という、目に見えないものを中心に扱っている。

* [人工知能](https://d.hatena.ne.jp/keyword/%E4%BA%BA%E5%B7%A5%E7%9F%A5%E8%83%BD)ではロボットの「脳の部分」を扱っている。（脳だけ、というわけではない）

* ロボットの研究者は[人工知能](https://d.hatena.ne.jp/keyword/%E4%BA%BA%E5%B7%A5%E7%9F%A5%E8%83%BD)の研究者というわけではない。

## 歴史

### ✅ 💻ENIAC

* 1946年、アメリカ ペンシルバニア大学。

* 世界初の汎用電子式コンピュータ。

    ![](https://upload.wikimedia.org/wikipedia/commons/6/6c/ENIAC_Penn1.jpg)

### ✅ ダートマス会議

* 1956年、アメリカで開催。

* 🎩ジョン・マッカーシーが初めて「人工知能（AI）」という言葉を使った。

* 世界初の人工知能プログラムといわれる💻[ロジック・セオリスト](https://ja.wikipedia.org/wiki/Logic_Theorist)のデモを実施した。

    ![](https://miro.medium.com/max/1000/0*8MW8iP2QC_WNhmiW)

### ✅ 第１次AIブーム

* **推論・探索** が中心。

* **トイ・プロブレム（おもちゃの問題）** は解けても、現実の問題は解けないことが判明。

    ⇒ 失望へ

### ✅ 第２次AIブーム

* 💻**エキスパートシステム**が流行し、[ナレッジエンジニア](https://www.weblio.jp/content/%E3%83%8A%E3%83%AC%E3%83%83%E3%82%B8%E3%82%A8%E3%83%B3%E3%82%B8%E3%83%8B%E3%82%A2)が必要とされた。

    ```
    ナレッジエンジニアとは、人工知能（AI）を応用したシステム構築を専門とする技術者（エンジニア）のことである。（引用）
    ```

* 日本

    💻**第五世代コンピュータ**という大型プロジェクトを推進、エキスパートシステム等に取り組んだ。

* 知識の蓄積・管理は大変！ということに気づく。

    ```
    第五世代コンピュータとは、通商産業省（現経済産業省）が1982年に立ち上げた国家プロジェクトの開発目標である。（引用）
    ```

    ⇒ 失望へ

### ✅ 第３次AIブーム

* **機械学習・特徴表現**が中心。

* ビッグデータによる**機械学習**、特徴量による**ディープラーニング（深層学習）** が流行。

# ２．📘人工知能をめぐる動向

# 2-1.📘探索・推論

## 探索・推論の手法

### ✅ 探索木

* 幅優先探索

    最短距離の解が必ずわかる。すべてを記憶するためメモリ容量が必要。

    ![](https://upload.wikimedia.org/wikipedia/commons/b/bc/Breadth-first-tree.png)

* 深さ優先探索

    メモリは少なめでよいが、最短距離が必ずわかるわけではない。

    ![](https://upload.wikimedia.org/wikipedia/commons/5/5d/Depth-first-tree.png)

### ✅ [ハノイの塔](https://ja.wikipedia.org/wiki/%E3%83%8F%E3%83%8E%E3%82%A4%E3%81%AE%E5%A1%94)

* 以下のルールに従ってすべての円盤を右端の杭に移動させられれば完成。

    * 3本の杭と、中央に穴の開いた大きさの異なる複数の円盤から構成される。

    * 最初はすべての円盤が左端の杭に小さいものが上になるように順に積み重ねられている。

    * 円盤を一回に一枚ずつどれかの杭に移動させることができるが、小さな円盤の上に大きな円盤を乗せることはできない。

    ![](https://upload.wikimedia.org/wikipedia/commons/6/60/Tower_of_Hanoi_4.gif)

### ✅ ロボットの行動計画

* [プランニング](https://ja.wikipedia.org/wiki/%E8%87%AA%E5%8B%95%E8%A8%88%E7%94%BB)

    * オフラインプランニング・静的プランニング

        周囲の状況が既知で、その構造がよく理解されている場合に、行動の計画や戦略をあらかじめ組み立てて(計算して）おくこと。

    * オンラインプランニング・動的プランニング

        未知の環境において、周囲の状況が明らかになるにつれて行動の計画や戦略を修正すること。

    * リプランニング

        計画・戦略を修正すること。

* STRIPS

    * Stanford Research Institute Problem Solver

    * 自動計画に関する人工知能の一種。

    * 前提条件、行動、結果を記述する。

* SHRDLU

    * 1970年、スタンフォード大学、🎩テリー・ウィノグラード。

    * 英語の指示により画面上の積み木を動かす。

    * 成果はCycプロジェクトに引き継がれている。

    * 【Youtube】SHRDLU in Action

        [![](https://img.youtube.com/vi/bo4RvYJYOzI/0.jpg)](https://youtu.be/bo4RvYJYOzI "SHRDLU in Action")
    
### ✅ ボードゲーム

* 1996年、💻**IBM DeepBlue（ディープブルー）。「[力任せの探索](https://ja.wikipedia.org/wiki/%E5%8A%9B%E3%81%BE%E3%81%8B%E3%81%9B%E6%8E%A2%E7%B4%A2)」だったが、チェスの世界チャンピオンを破った。

    ```
    力まかせ探索（Brute-force search）またはしらみつぶし探索（Exhaustive search）は、単純だが非常に汎用的な計算機科学の問題解決法であり、全ての可能性のある解の候補を体系的に数えあげ、それぞれの解候補が問題の解となるかをチェックする方法である。（引用）
    ```

* 2012年、💻ボンクラーズ が将棋において永世棋聖に勝利。

* 2013年、💻ponanza が将棋において現役プロ棋士に勝利。

* 2016年、💻AlphaGo（アルファ碁）が韓国のプロ棋士に勝利。

    ディープラーニングが使われた。

    ![](https://tech-camp.in/note/wp-content/uploads/alphago-1024x519.png)

* 2017年、💻elmo が世界コンピュータ将棋選手権において ponanza に勝利。elmo 同士の対戦を行うことで学習を行った。

### ✅ コスト

* 効率よく探索するため、時間や費用といったコストの概念を取り入れている。

* ヒューリスティックな知識を利用して探索を短縮することができる。

    ※ヒューリスティック：経験則の、試行錯誤的な

### ✅ [Mini-Max法](https://ja.wikipedia.org/wiki/%E3%83%9F%E3%83%8B%E3%83%9E%E3%83%83%E3%82%AF%E3%82%B9%E6%B3%95)

* ゲーム戦略で利用される。

* 想定される「最大の損害」が最小になるように決断を行う戦略のこと。

* 自分の番はスコア最大、相手の番はスコア最小になるような戦略をとる。

* この手法は全探索を行うため効率が悪い。

# 参考

以下のサイトからの情報をもとに個人でまとめました。

* [【資格試験対策】ディープラーニングG検定【キーワード・ポイントまとめ】](https://sik-bug.hatenablog.com/entry/2020/05/30/103038)




