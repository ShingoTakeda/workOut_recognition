# workOut_recognition
行動認識疑似術を用いた自重トレーニングの自動認識

## 対象行動
01. 腕立て伏せ
02. 腹筋(クランチ)
03. レッグレイズ
04. プランク
05. バードドッグ
06. ヒップリフト
07. スクワット
08. フロントランジ
09. ランニング
10. 片足ドロップジャンプ
11. 連続ジャンプ

## 使用センサ
加速度センサ計5つ(両手首、両足首、腰の中央)
サンプリングレート200Hz

## prediction.ipyb
行動推定用スクリプト。
ファイルベースの認識を想定。１行動分のcsvファイルを入力とした時に、推定結果として、その行動の名前をcsvファイルで出力する。
実行すると学習済みモデル(trained_model.sav)が読み込まれ、入力したファイルに対して推定を行い、その結果がcsvファイルとして同フォルダ内estimation_resultというフォルダの中に出力される。
出力されたcsvファイル名は実行した日時となっており、ファイル内には出力した日時、推定された行動名が記入される。

## training_model.ipynb
モデル学習用スクリプト。
収集したデータを用いて行動認識モデルを学習する。

## trained_model.sav
学習済みモデル。
prediction.ipybで読み込まれ入力ファイルから行動を推定する。
