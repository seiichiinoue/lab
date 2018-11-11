## 浅井ゼミ
### 説明
- 2018年11月21日に創価大学で行われる，経済学部ゼミ対抗論文大会における論文作成における分析を担当．
	- [過去の実施例](https://www.soka.ac.jp/economics/news_economics/2017/11/2552/)
- 論文のテーマを，"学内ローソンの行列を解消する施策"とし，学部生を対象としたアンケートを実施．
- 本分析はその結果の可視化と，データマイニングを目的としている．

### file
- ゼミ対抗論文大会におけるアンケート結果の分析(完成版)

### 概要

- 創価大学に所属する学生に学内ローソンにおける行列に関するアンケートを行い，そのデータに基づいて分析をしていく．
- 有効回答数 : 412（仮）


#### データ成形
- アンケートにある質問から，有効なデータだけを切り取り，分析可能な数値データに変換する
- 各分析手法にマッチしたラベル，特徴量の作成を行う．

#### 分析手法
- 主成分分析
- カーネル主成分分析; カーネルトリック
- 因子分析
    - 主成分分析における共分散行列の固有値，固有ベクトルを使用し，因子負荷量を算出し，主成分の意味を考察する
- ロジスティック回帰
- サポートベクターマシン
- ガウスカーネルサポートベクターマシン
- 決定木学習

#### 分析概要
- 分類問題の目標は，「電子マネーを使う/使わない」，「キャッシュレス決済を使う/使わない」
- 分類問題を解く際に，モデルの使い分けと，分析の容易さを考慮して，3種類のラベルデータを3つの手法に分けて分析を行う


- 1 キャッシュレス決済を使用したことがあり，電子マネーを持っている人 / キャッシュレス決済を使用したことがないかつ電子マネーを持っている人の2値分類

- 2 キャッシュレス決済を使用したことがあり，電子マネーを持っていない人 / 電子マネーを持っていない人の2値分類

- 3 キャッシュレス決済を使用したことがあり，電子マネーを持っている人 / キャッシュレス決済を使用したことがないかつ電子マネーを持っている人 / 電子マネーを持っていない人の3値多クラス分類
