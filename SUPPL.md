# 補足情報  

本書の補足情報を掲載しております。  

## P.30: リスト2.4.4： GUIへ関数の追加

tk.Button()の引数へ「command = run_func」を追加する際は、,(コンマ)で区切ることを忘れないようにしてください。
本書中では説明が不十分でしたが、引数内の各引数間は、必ず,(コンマ)で区切る必要があります。  

```python
# Runボタン
run_button = tk.Button(root, text = "Run", command = run_func)
run_button.place(x = 110, y = 30)
```
,(コンマ)を忘れると、エラーが発生するので注意してください。 Python初心者がエラーを起こしがちな箇所です。  
サンプルファイル([Chapter_2.ipynb](./Chapter_2/Chapter_2.ipynb))にも補足情報を追加しました。
</br>
</br>
## P.178: リスト 6.1.15： x 軸方向のスクロールバー

x軸方向のスクロールバーを実際にテストしたい場合は、以下の箇所を変更してください。  

```python
# 変更前
txtbox = tk.Text(frame, width = 60, height = 20)
```
```python
# 変更後「wrap = "none"」の追加
txtbox = tk.Text(frame, width = 60, height = 20, wrap = "none")
```
Textウイジットのwrap = "none"オプションは、テキストボックス中の長い行の折り返しを無効にするためのものです。  
テキストボックスの幅以上の文字列を入力すると、x軸方向のスクロールバーが動作します。  
サンプルファイル([Chapter_6-1.ipynb](./Chapter_6/Chapter_6-1.ipynb))にも補足情報を追加しました。
