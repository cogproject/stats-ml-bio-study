# 統計・機械学習 独学カリキュラム(Google Colab + GitHub)

1日30分〜週3時間のペースで進める計画。
題材:公開の遺伝子発現データ(RNA-seq)を中心に使う。

## 使うデータ
| データ | 中身 | 使い道 | 出典 |
|---|---|---|---|
| UCI「Gene expression cancer RNA-Seq」 | TCGA のがん患者 801 人 × 遺伝子 20,531 個の発現量。がんの種類 5 つ(BRCA, KIRC, COAD, LUAD, PRAD)のラベル付き | 可視化、PCA、クラスター分析、分類(決定木・RF) | https://archive.ics.uci.edu/dataset/401/gene+expression+cancer+rna+seq |
| GEO の公開データ(第2段階) | NCBI の遺伝子発現データベース | 生データに近い形の扱い、正規化の理解 | https://www.ncbi.nlm.nih.gov/geo/ |
| scikit-learn 付属データ(補助) | 糖尿病データなど | 回帰の練習(遺伝子データは回帰向きでないため) | https://scikit-learn.org/stable/datasets/toy_dataset.html |

## 第1段階:入門(2026年11月、1回30分 × 10回)
ねらい:公開の RNA-seq データで、主成分分析とクラスター分析まで手を動かす。

| 回 | 日付 | 内容 | 成果物 |
|---|---|---|---|
| 0 | 11/15 | GitHub リポジトリ作成、Colab から開けることを確認 | README |
| 1 | 11/16-17 | データの読み込みと形の確認、ラベルの数、発現量の分布(ヒストグラム)、log 変換 | `01_data_overview.ipynb` |
| 2 | 11/18-19 | 遺伝子どうしの相関、ヒートマップ。相関と因果の違いを言葉でまとめる | `02_correlation.ipynb` |
| 3 | 11/20-21 | 主成分分析(PCA):標準化 → 2次元に圧縮 → がんの種類で色分け | `03_pca.ipynb` |
| 4 | 11/22-23 | クラスター分析:k-means と階層クラスタリング。正解ラベルと比べる | `04_clustering.ipynb` |
| 5 | 11/24-25 | README に「やったこと・分かったこと・次にやること」をまとめる | README 更新 |


## 第2段階:2026年12月〜2027年3月(週3時間 × 約16週)
gacco「"わかる・使える"統計解析プログラミング」(2027-01-12 開講)の範囲を先取りし、バイオの題材で深める。
講座の範囲は開講前に公式ページで確認する:https://gacco.org/stat-japan3/

| 期間 | テーマ | 内容 | 参照 |
|---|---|---|---|
| 12月 1-2週 | 統計の基礎:検定 | t 検定、分散分析(R 経験の Python 版)、効果量。2群の発現差 | scipy.stats https://docs.scipy.org/doc/scipy/reference/stats.html |
| 12月 3-4週 | 多重比較 | 2万遺伝子を一度に検定すると何が起きるか。Bonferroni と FDR(Benjamini-Hochberg) | statsmodels multipletests https://www.statsmodels.org/stable/generated/statsmodels.stats.multitest.multipletests.html |
| 1月 1-2週 | 回帰 | 単回帰・重回帰、残差、正則化(Ridge/Lasso) | https://scikit-learn.org/stable/modules/linear_model.html |
| 1月 3-4週 | PCA を深める | 寄与率、負荷量(どの遺伝子が効いているか) | https://scikit-learn.org/stable/modules/decomposition.html#pca |
| 2月 1-2週 | 決定木 | がんの種類の分類、訓練・テスト分割、交差検証、過学習 | https://scikit-learn.org/stable/modules/tree.html |
| 2月 3-4週 | ランダムフォレスト | 精度比較、特徴量の重要度(重要な遺伝子) | https://scikit-learn.org/stable/modules/ensemble.html#forest |
| 3月 | まとめ+NGS の入口 | GEO のカウントデータで正規化から PCA まで。RNA-seq 解析の流れ(FASTQ → アライメント → カウント)を図で整理 | GEO https://www.ncbi.nlm.nih.gov/geo/ 、DESeq2 解説 https://bioconductor.org/packages/release/bioc/vignettes/DESeq2/inst/doc/DESeq2.html |

gacco 受講中は、講座の演習を `notebooks/gacco/` に置き、同じ手法をバイオデータで試した版を並べる。

## 注意
- 本カリキュラムの説明は要約です。手法の定義は各リンク先の公式ドキュメントで確かめてください。
- TCGA データは研究利用の公開データですが、UCI 版は加工済み(正規化済みの発現量)で、生のカウントではありません。
