# dvorakjp-romantable
Google日本語入力用デフォルトのローマ字テーブルをベースに、DvorakJPのマッピングを行ったローマ字テーブルです。

DvorakJP自体についてはこちら: [DvorakJP](http://www7.plala.or.jp/dvorakjp/)

本リポジトリのローマ字テーブルは、さらに一部カスタマイズしていますが、通常のDvorakJP用のローマ字テーブルとして利用する分にはほぼ差し支えない設定になっています。

### Google日本語入力のデフォルトローマ字テーブル(2015-10-11現在のもの) について

通常のローマ字テーブルに加えて以下の特徴があります。

1. `z*`キーによる記号入力
  - `zh`: `←`, `zj`: `↓`などの記号入力が可能
1. 訓令式以外のローマ字テーブル
  - `f*`, `ch*`, `ts*`などの一般的なヘボン式ローマ字テーブルの追加
  - `kya`: `きゃ`などの`y`を利用した拗音の他に、`twa`: `とぁ`などの`w`拗音の追加
1. `t'u`: `とぅ`などの`'`を利用した拗音が追加
  - ただし、分かりづらい上に`twu`: `とぅ`など、他の入力でも代替可能な拗音もあり、利用価値が不明

デフォルトローマ字テーブルはこちら: [romantable_original.txt](https://github.com/shinespark/dvorak-romantable/blob/master/romantable_original.txt)

### DvorakJPについて

左手ホームポジションに母音がすべて揃っているDvorak配列を、日本語入力でも使いやすいように更に拡張するローマ字テーブルです。
右手と左手を交互に打鍵可能なよう、以下の特徴を持っています。

1. `k*`のキーを`c*`でも利用可能
1. 拗音入力時に利用する`y`キーの代わりに、`h`, または`n`キーが利用可能
  - 多様する子音が右手で入力可能に
1. 二重母音拡張と撥音拡張を追加
  - 連続する母音入力(左手での連続打鍵回数)を低減

参照: [DvorakJP - 日本語入力用拡張Dvorak](http://www7.plala.or.jp/dvorakjp/dvorakjp.htm)

### 本ローマ字テーブルについて

Google日本語入力とDvorakJPのローマ字テーブルのマージにあたって、以下の一部変更を行っています。
以下の内容は通常のDvorakJPとして利用する分には、コンビネーションキーを利用した`qy*`, `xn*`以外には支障はありません。

1. Google日本語入力の `z*`キーによる記号の入力を、`;*`に変更
  - ざ行の入力と競合する為、Qwerty時の`z`のキーに位置する`;`に置換。
1. Google日本語入力の `ch*`, `tw*` などにも二重母音拡張と撥音拡張を追加
  - 元のローマ字テーブルもほぼ残している為、`t*`が多くなっています。
    - `tha`: `てゃ`, `tna`: `ちゃ`, `tsa`: `つぁ`, `twa`:`とぁ`
1. Google日本語入力の `t'u`: `とぅ`などの`'`を利用した拗音入力の削除
  - 分かりづらいので。入力の際は`two`: `とぅ`などを利用してください。
1. DvorakJP 0.2β時の`p`キーに二重母音拡張`uu`を復活
  - Google日本語入力では連続同文字打鍵での「っ」が入れられない問題は発生しない(はず)
  - 参照: [DvorakJP - 前バージョンからの改定について](http://www7.plala.or.jp/dvorakjp/)
1. DvorakJPの`q`のコンビネーションの削除と、`k`のコンビネーション有効化
  - Google日本語入力に`qy*`が存在しないため、`q`のコンビネーション用のマッピングを行っていません。
  - DvorakJPではか行の入力の際に`k`を利用した場合のコンビネーションキーは存在しませんが、`k`でもか行が入力できることから、`k`でもコンビネーションキーを利用した二重母音拡張と拗音拡張が利用可能にしています。
1. DvorakJPの`p`, `j`, `k`のコンビネーションキーは`h`,`n`どちらでも入力可能に
  - 左手側の子音入力時の拗音入力時に、右手薬指または人差し指どちらでも入力変更になります。
1. DvorakJPの`x`のコンビネーションキーを`h`に
  - Google日本語入力では`xn`: `ん`の為、`xn*`のキーを撤廃しています。
