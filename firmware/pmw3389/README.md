# PMW3389 実験用ファームウェア

通常のLotusOrbはPMW3360用ファームウェアを使用します。このフォルダはPMW3389を搭載した実験用構成向けです。

現在はビルド待ちで、UF2はまだ格納していません。実機での動作も未確認です。現行基板と同じSPI配線を前提にしています。

| 種類 | ソース |
| --- | --- |
| 3389通常版 | [feat/pmw3389](https://github.com/yubinagasaru/vial-qmk/tree/feat/pmw3389) |
| 3389・左スクロール量を減らした版 | [feat/pmw3389-scroll-reduced](https://github.com/yubinagasaru/vial-qmk/tree/feat/pmw3389-scroll-reduced) |

左スクロール調整版は、倍率を縦横1、左専用しきい値を29に設定しています。左1600 CPI、右の初期値2800 CPIを加味し、SCR＋右トラックボールのスクロール量に近づけています。

3389へセンサーを交換する場合は左右とも3389用ファームウェアが必要です。スクロール調整の処理はUSBを接続する側で行います。
