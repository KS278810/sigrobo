# SigRobo Web版

<https://ks278810.github.io/sigrobo/>

CSV をドロップして課題を選ぶだけで、時系列の回帰モデルを同じ条件で比べるツール
**SigRobo** の Web 版です。ブラウザ内で完結し、Pyodide で動きます。
データがどこかへ送信されることはありません。

## この版で動くもの

- 課題 A 仮想センサー、B 予測、C 系列から 1 つの値、の 3 つです
- 動くのは、ブラウザの中で計算できる手法だけです。サーバー版にだけあるのは、課題 A の lstm、gru、tcn、chronos2、課題 B の dlinear、patchtst、itransformer、chronos2、課題 C の rocket、drcif です
- 入力は CSV のみです
- ets、arima、arimax の予測は、サーバー版と少し違います。ets は小数第 5 位から、arima と arimax は、サンプル 2 本の測定で、予測の幅に対する差が最大でそれぞれ 3.6e-3 と 1.4e-5 でした。係数を求める最適化が、環境によって別の点で止まるためです
- ONNX は linear、arx、narx、lightgbm、arimax、persistence、seasonal_naive、ets、arima、theta、dummy、summary_lightgbm、minirocket で書き出せます。ほかのモデルの ONNX は、サーバー版で書き出します

## このリポジトリについて

**ビルド済みの配布物だけ**を置いています。ソースコードは非公開の開発リポジトリ側に
あり、ここへは難読化を通した成果物が配置されます。

- 中身は自動生成なので、**直接編集しないでください**。次の配置で上書きされます
- 履歴は持ちません。更新のたびに単一のコミットを差し替えます

## ライセンス

CC BY-NC 4.0、表示と非営利。教育と研究での利用は自由です。商用利用をご希望の場合は
[Issues](https://github.com/KS278810/sigrobo/issues) からご相談ください。
