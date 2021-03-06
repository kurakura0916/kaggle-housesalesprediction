# [WIP]kaggle-housesalesprediction

## 概要
kaggleの[House Sales in King County, USA](https://www.kaggle.com/harlfoxem/housesalesprediction)のデータセットを用いた住宅の販売価格予測

## データセットの説明
シアトル、キング群にある住宅の情報を表したデータセット。

| カラム名 | データ型 | 説明 |
|:---|:---|:---|
|id |numeric |各住宅につけられた固有のid |
|date |character |販売日 |
|price |numeric |販売価格 |
|bedrooms |integer |ベッドルームの数 |
|bathrooms |numeric |バスルームの数 |
|sqft_living |integer |リビングルームの広さ |
|sqft_lot |integer |駐車場の広さ |
|floors |numeric |階数 |
|waterfront |integer |ウォーターフロントかどうか（0 or 1） |
|view |integer |景色の種類（0~4） |
|condition |integer |住宅の状態（1~5） |
|grade |integer |住宅のグレード（1~13） |
|sqft_above |integer |地上階の広さ |
|sqft_basement |integer |地下の広さ |
|yr_built |integer |建築年 |
|yr_renovated |integer |リノベーションの年 |
|zipcode |integer |郵便番号 |
|lat |numeric |緯度 |
|long |numeric |経度 |
|sqft_living15 |integer |近所15件の平均のリビングの広さ |
| sqft_lot15|integer |近所15件の駐車場の広さ |

## 環境
Python 3.6.4

## アルゴリズム
- 線形回帰
- リッジ回帰
- ロッソ回帰
- 決定木（回帰木）
- ランダムフォレスト（回帰木）

## 評価指標
RMSE（平均二乗平方根誤差）

## 作業手順
1. 欠損値の確認
2. データ探索
3. 説明変数の作成
4. 訓練データとテストデートに分割
5. 予測モデルの作成
6. テストデータへの当てはめとRMSEの算出

- 線形回帰の場合

7. 回帰係数を確認するために説明変数を正規化
8. 回帰係数の可視化
9. 3へ戻りモデルの調整

- 決定木の場合

7. 木の深さを調整しRMSEを算出

- ランダムフォレストの場合

7. 変数増加法により変数の選択
8. クロスバリデーションによるハイパーパラメータの調整
9. 5に戻りRMSEを算出
