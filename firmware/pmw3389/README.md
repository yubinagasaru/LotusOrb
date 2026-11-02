# PMW3389 実験用ファームウェア

通常のLotusOrbはPMW3360用ファームウェアを使用します。このフォルダはPMW3389を搭載した実験用構成向けです。現行基板と同じSPI配線を前提としています。ローカルビルドは確認済みですが、実機での動作は未確認です。

| 種類 | ファイル |
| --- | --- |
| 3389通常版・左用 | [lotusorb_vial_left.uf2](lotusorb_vial_left.uf2) |
| 3389通常版・右用 | [lotusorb_vial_right.uf2](lotusorb_vial_right.uf2) |
| 3389・左スクロール量を減らした版・左用 | [lotusorb_vial_left_scroll_reduced.uf2](lotusorb_vial_left_scroll_reduced.uf2) |

3389へセンサーを交換する場合は左右とも3389用ファームウェアが必要です。

左スクロール調整版は、倍率を縦横1、左専用しきい値を29に設定しています。左1600 CPI、右の初期値2800 CPIを加味し、SCR＋右トラックボールのスクロール量に近づけています。通常3389版と比べて、同じボール移動量に対する縦スクロールは約57％、横は約86％になります。

ここに置いているスクロール調整版は、左にUSBを接続して使う場合の左用UF2です。スクロール変換はUSB接続側で処理されます。

## ビルド元

- 通常版: [feat/pmw3389](https://github.com/yubinagasaru/vial-qmk/tree/865eb71d17a081250cefe969f483fff712bc5094)
- 左スクロール調整版: [feat/pmw3389-scroll-reduced](https://github.com/yubinagasaru/vial-qmk/tree/8ed839718ec576bb660baa4e9452a837f39066cc)
- ビルド日: 2026-11-02
- ビルド環境: Windows / QMK MSYS、ARM GCC 12.2.0
- ビルドコマンド: `make lotusorb:vial_left`、`make lotusorb:vial_right`

