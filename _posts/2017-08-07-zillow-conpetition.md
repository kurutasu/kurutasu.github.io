---
layout: post
title: 作成中）KaggleのZillow Prizeに挑戦
updated: 2017-08-07 18:00 
categories:
 - machine learning
---

[KaggleのZillow Prize](https://www.kaggle.com/c/zillow-prize-1)に挑戦する．課題は不動産価格の予測であり，賞金は総額1億円以上（$1,200,000）．

# 1. 背景

## 1.a Kaggle

[Kaggle](https://www.kaggle.com/)とは，データサイエンティストのプラットフォームである．様々なコンペティションが開催されており，データサイエンティストの腕試しの場として広く認知されている．Kaggleへの参加方法については，[Kaggle事始め](http://qiita.com/taka4sato/items/802c494fdebeaa7f43b7)が詳しい．

## 1.b Zillow

[Zillow](https://www.zillow.com/)とは，オンライン不動産データベースを運営するアメリカの企業．アメリカ全土の1億件以上の物件情報を有し，Zestimateと呼ばれる価格見積もりサービスを持つ．

## 1.c Zillow Prize

[Zillow Prize](https://www.kaggle.com/c/zillow-prize-1)は，Zillowが2017年5月に開始したコンペティション．課題は不動産価格の予測で，賞金は総額1億円以上（$1,200,000）．本コンペティションは，qualifying roundとprivate roundからなる．private roundは，qualifying roundの上位100チームのみに対し2018年1月1日から実施される．

[Data](https://www.kaggle.com/c/zillow-prize-1/data)や[Rules](https://www.kaggle.com/c/zillow-prize-1/rules)の詳細は以下．

### Data

本コンペティションの目的は，Zestimateと実際の売値（$$SalePrice$$）の対数誤差を予測すること．対数誤差は以下で定義される．

$$
\begin{align*}
logerror = log(Zestimate) - log(SalePrice) \tag{1}
\end{align*}
$$

具体的には，2017年秋における$$logerror$$を予測する．不動産価格は公開情報なので，取引が始まる前に，モデルの提出を打ち切る．

訓練データとして，2016年の三箇所（Los Angeles，Orange and Ventura，California）の全ての不動産データが提供される．訓練データは2016年10月15日以前の全ての取引と，それ以降のいくつかの取引を含む．public leaderboardのテストデータは，2016年10月15日から同年12月31日までのものである．private leader boardのテストデータは，2017年10月15日から同年12月15日まで（この期間をsales tracking periodと呼ぶ）のものである．つまり，参加者は次の６時点における全ての不動産に対して予測を行う必要がある．

* October 2016 (201610)
* November 2016 (201611)
* December 2016 (201612)
* October 2017 (201710)
* November 2017 (201711)
* December 2017 (201712)

当該期間において取引が行われなかった不動産は，scoreの計算に利用されない．31日間のうち，複数回の取引があった場合は，最初の適切な取引をscoreの計算に用いる．

以下は各ファイルの概要．
* `properties_2016.csv`：2016年の全ての不動産情報．
* `properties_2017.csv`：2017年の全ての不動産情報．2017年10月2日に公開予定．
* `train_2016.csv`：2016年1月1日から2016年12月31日までの取引情報．
* `train_2017.csv`：2017年1月1日から2017年9月15日までの取引情報．2017年10月2日に公開予定．
* `sample_submission.csv`：提出用のサンプルファイル．

### Rules

重要そうなものだけ抜粋．

* チーム外に，コードを共有してはならない．ただし，全参加者に共有するのはOK．
* 1チーム最大3人まで．
* 1日5回まで提出可能．最終的に，最大2つの予測結果を投稿可能．
* 賞金総額：$1,200,000
  * 第1ラウンド総額：$50,000
    * 1位：$25,000
    * 2位：$15,000
    * 3位：$10,000
  * 第2ラウンド総額：$1,150,000
    * 1位：$1,000,000
    * 2位：$100,000
    * 3位：$50,000

# 2. 情報収集

[Kernel](https://www.kaggle.com/c/zillow-prize-1/kernels)で情報収集．

# 3. 実装

# 参考

* [Kaggle事始め](http://qiita.com/taka4sato/items/802c494fdebeaa7f43b7)：とても丁寧なKaggle入門．
* [No Free Hunch](http://blog.kaggle.com/)：Kaggle公式ブログ．コンペ優勝者のモデルが公開されている．