# BF-026

HK322 / HK326 Music Player

メロディIC HK322, HK326 の演奏を楽しめるプリント基板です。
データシートの応用回路を実装できます。
単三乾電池 2 本を使用します。

# 1.機能

- 基板上に小型スピーカーがあり、単体で演奏できます。
- 音量を調整できます。
- LED がテンポに合わせて点滅します。
- モーターの接続端子があり、演奏中に回せます。
- ボタン操作の動作モードを選べます。
- スピーカー信号をピンヘッダから外部に取り出せます。

# 2.組み立て

組み立てには、はんだ付けが必要です。はんだ、はんだごて、ニッパー等が必要です。
ネジ止めやターミナルブロックへの導線の接続には、ドライバー等が必要です。

背の低い部品からプリント基板にはんだ付けするのがコツです。
LED には極性があり、リード線の短い方がマイナスです。プリント基板上の K (Kathode) マークがマイナス側です。
電解コンデンサには極性があり、リード線の短い方がマイナスです。

SPEAKER 表示のピンヘッダー (4p) に、ショートピン 2 本をプリント基板の長い方向に並べて挿します。
外部スピーカー等を使用する場合は、ショートピンを取り外して IC に近い方のピン 2 本から信号を取り出します。

# 3.動作

動作モードは、ピンヘッダー (6p) に対してショートピン 2 本で設定します。


| MODE | SL | 動作モード　| 説明　|
|:--:|:--:|:---|:---|
| VSS | VSS | Play All Songs　| TG ボタンを押すと、全曲を 1 曲目から 1 回演奏します。 |
| VSS | VDD | One Shot Re-Trigger | TG ボタンを押すと、1 曲目から 1 曲を演奏します。曲の途中で TG ボタンを押すと次の曲に移ります。TG ボタンを押し続けた場合、曲が終わる毎に次の曲を演奏します。 |
| VDD | VSS | One Shot Non Re-Tregger　| TG ボタンを押すと、1 曲目を最後まで演奏します。次に TG ボタンを押すと、次の曲を最後まで演奏します。 |
| VDD | VDD | On/Off Switch　| TG ボタンを押すと、全曲を 1 曲目から 1 回演奏します。演奏中に TG ボタンを押すと演奏を停止します。 |
| VSS | VSS | TG = VSS: Power On/Off　| TG を VSS に短絡すると、電源オンで全曲を 1 曲目から 1 回演奏させることができます。|

# 4.参考資料

メロディ IC の機能、動作の詳細、曲目の違いなどは、リンク先を参照ください。

- HK322, HK326 メーカー:

[Honsitak Electronics Co., Ltd.] https://www.honsitak-taiwan.com/products03.htm

- 小売：株式会社秋月電子通商

[HK322-1] https://akizukidenshi.com/catalog/g/gI-15483/

[HK322-3] https://akizukidenshi.com/catalog/g/gI-15484/

[HK322-6] https://akizukidenshi.com/catalog/g/gI-15485/

[HK326-2] https://akizukidenshi.com/catalog/g/gI-15486/


# 5.提供元

BotanicFields, Inc.

[twitter] https://twitter.com/botanicfields

[facebook] https://www.facebook.com/botanicfields

[Qiita] https://qiita.com/BotanicFields

[GitHub] https://github.com/botanicfields

[SwitchScience] https://www.switch-science.com/catalog/list/1084/
