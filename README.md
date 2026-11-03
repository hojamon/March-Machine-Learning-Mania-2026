# March Machine Learning Mania 2026

Kaggle「[March Machine Learning Mania 2026](https://www.kaggle.com/competitions/march-machine-learning-mania-2026)」の解法です。
NCAAバスケットボールトーナメント（男女）の勝敗確率を予測するコンペです。

## 結果

**181位 / 3,462チーム（銅メダル）**

## 解法の概要

- 特徴量：シーズン成績、対戦相手で補正したスタッツ、直近10試合の調子、Elo、SOS、カンファレンスの強さ、シード別の過去勝率、Massey Ordinals（男子のみ）
- モデル：LR / GBM / XGBoost / LightGBM のアンサンブル（男女別に学習）
- 直近のシーズンほど重みを大きくして学習（decay = 0.97）
- goto_conversion で確率を補正
