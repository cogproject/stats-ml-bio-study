# stats-ml-bio-study
**本物の遺伝子データを使って、統計と機械学習を一から学ぶノート集**です。
Google Colab(ブラウザだけで Python が動くサービス)で、だれでもそのまま動かせます。

## このリポジトリでできること
- がんの患者さんの遺伝子データ(公開データ)を、グラフにしてながめる
- 「似ている」「ちがう」を数字で確かめる(相関・検定)
- たくさんのデータを、すっきりまとめる(主成分分析・クラスター分析)
- データから予測する(回帰・決定木・ランダムフォレスト)

解説は、中学生でも読めることを目指して書いています。

## ノート一覧
| # | ノート | 内容 | 開く |
|---|---|---|---|
| 01 | [データをながめてみよう](notebooks/01_data_overview.ipynb) | 表の大きさ、ヒストグラム、箱ひげ図 | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/cogproject/stats-ml-bio-study/blob/main/notebooks/01_data_overview.ipynb) |
| 02 | [似た動きをさがそう(相関)](notebooks/02_correlation.ipynb) | 散布図、相関係数、ヒートマップ、相関と因果のちがい | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/cogproject/stats-ml-bio-study/blob/main/notebooks/02_correlation.ipynb) |
| 03 | データをまとめて地図にしよう(主成分分析) | | 準備中 |
| 04 | なかま分けしよう(クラスター分析) | | 準備中 |

## 使い方
1. 上の表の「Open in Colab」ボタンを押す(Google アカウントが必要です)
2. 上のセルから順に ▶ を押して実行する

## 使っているデータ
- UCI Machine Learning Repository「Gene expression cancer RNA-Seq」(元は米国 TCGA プロジェクト、CC BY 4.0)
  https://archive.ics.uci.edu/dataset/401/gene+expression+cancer+rna+seq
- データはこのリポジトリには入れず、ノートの中で配布元からダウンロードします。

## そのほか
- 学習の計画:[curriculum.md](curriculum.md)
- 学習の記録:[logs/](logs/)
- 解説に誤りがあれば、Issue で教えてもらえるとうれしいです。手法の正確な定義は、各ノートに載せた公式ドキュメントで確かめてください。
