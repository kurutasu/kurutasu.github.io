* CirckeCI の説明

アジャイル開発が定着してきた

継続的インテグレーション
CI：
共有リポジトリにコミットを積み重ね、全てのコミットをトリガーにしてビルドとテストを繰り返すこと

why
チームの満足度や不安度を解消させる

1. 解決される問題

* 全てのコミットに対してCIする
    * 早い段階でバグを発見させる
    * 設定で制御可能
* 静的解析などでの標準化
    * コード品質UP
* テストに失敗したコードのマスターブランチへの適用ブロック


2010

継続的デリバリー
CD
- Continuous Delivery

    常にリリース可能な状態を維持する = デプロイはしてない

- Continuous Deployment
    自動でステージング・本番環境へデプロイする

question
1)CDをしている企業の利用している主な言語の割合

    * Tec系の会社がおおい
    * RubyやPHPが多い
    
    感触

2)CDのリポジトリのサイズ感