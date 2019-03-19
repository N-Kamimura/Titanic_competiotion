# Titanic: Machine Learning from Disaster

Kaggleの"Titanic: Machine Learning from Disaster"で上位5％に入った時のコードです。

以下の方針に従い、データを加工しています。


【特徴量の選択の方針】

　1.基本方針
<br>　　客室の等級、性別、子供であるかが最も重要なものであると判断しています。

　2.同乗者の人数
<br>　　独身者、同乗者が1人の男性、大家族の死亡率が高かったため、同乗者の数を要素として加えています。
<br>　　ただし、2人で乗船していても、片方が子供の場合、子供を1人にするわけにはいかないと仮定しています。
<br>　　そのため、子供と一緒に乗船しているかも要素として加えています。

　3.データの充足度
<br>　　生存者のデータは死亡者よりデータの充足率が高いので、各サンプルのNull値の数も特徴量に加えています。


【モデル】
<br>　　XGブーストを使用
<br>　　ハイパーパラメータはグリッドリサーチにより選定。

※使用した特徴量、ハイパーパラメータは"Config"ファイルをご参照ください。
