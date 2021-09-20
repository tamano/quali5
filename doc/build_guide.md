# ビルドガイド / Build Guide

* [材料 / Parts](#%E6%9D%90%E6%96%99--parts)
* [組み立て手順](#%E7%B5%84%E3%81%BF%E7%AB%8B%E3%81%A6%E6%89%8B%E9%A0%86)
    * [1. ダイオードをハンダ付けする / Solder diodes](#1-%E3%83%80%E3%82%A4%E3%82%AA%E3%83%BC%E3%83%89%E3%82%92%E3%83%8F%E3%83%B3%E3%83%80%E4%BB%98%E3%81%91%E3%81%99%E3%82%8B--solder-diodes)
    * [2. スイッチ用PCBソケットをハンダ付けする / Solder PCB Hot-swappable sockets](#2-%E3%82%B9%E3%82%A4%E3%83%83%E3%83%81%E7%94%A8pcb%E3%82%BD%E3%82%B1%E3%83%83%E3%83%88%E3%82%92%E3%83%8F%E3%83%B3%E3%83%80%E4%BB%98%E3%81%91%E3%81%99%E3%82%8B--solder-pcb-hot-swappable-sockets)
    * [3. ピンヘッダをハンダ付けする / Solder pin headers to PCB plate](#3-%E3%83%94%E3%83%B3%E3%83%98%E3%83%83%E3%83%80%E3%82%92%E3%83%8F%E3%83%B3%E3%83%80%E4%BB%98%E3%81%91%E3%81%99%E3%82%8B--solder-pin-headers-to-pcb-plate)
    * [4. ProMicroをハンダ付けする / Solder the ProMicro](#4-promicro%E3%82%92%E3%83%8F%E3%83%B3%E3%83%80%E4%BB%98%E3%81%91%E3%81%99%E3%82%8B--solder-the-promicro)
    * [5. リセットスイッチをハンダ付けする / Solder a reset switch](#5-%E3%83%AA%E3%82%BB%E3%83%83%E3%83%88%E3%82%B9%E3%82%A4%E3%83%83%E3%83%81%E3%82%92%E3%83%8F%E3%83%B3%E3%83%80%E4%BB%98%E3%81%91%E3%81%99%E3%82%8B--solder-a-reset-switch)
    * [6. OLEDにピンヘッダをハンダ付けする / Solder a pin header to an OLED](#6-oled%E3%81%AB%E3%83%94%E3%83%B3%E3%83%98%E3%83%83%E3%83%80%E3%82%92%E3%83%8F%E3%83%B3%E3%83%80%E4%BB%98%E3%81%91%E3%81%99%E3%82%8B--solder-a-pin-header-to-an-oled)
    * [7. OLEDをハンダ付けする / Solder the OLED to the the PCB plate](#7-oled%E3%82%92%E3%83%8F%E3%83%B3%E3%83%80%E4%BB%98%E3%81%91%E3%81%99%E3%82%8B--solder-the-oled-to-the-the-pcb-plate)
    * [8. スイッチとキーキャップをトッププレートにはめる / Attach switchs and keycaps to the top plate](#8-%E3%82%B9%E3%82%A4%E3%83%83%E3%83%81%E3%81%A8%E3%82%AD%E3%83%BC%E3%82%AD%E3%83%A3%E3%83%83%E3%83%97%E3%82%92%E3%83%88%E3%83%83%E3%83%97%E3%83%97%E3%83%AC%E3%83%BC%E3%83%88%E3%81%AB%E3%81%AF%E3%82%81%E3%82%8B--attach-switchs-and-keycaps-to-the-top-plate)
    * [9. トッププレートをPCB基板にはめ込む / Mount the top plate over the PCB board](#9-%E3%83%88%E3%83%83%E3%83%97%E3%83%97%E3%83%AC%E3%83%BC%E3%83%88%E3%82%92pcb%E5%9F%BA%E6%9D%BF%E3%81%AB%E3%81%AF%E3%82%81%E8%BE%BC%E3%82%80--mount-the-top-plate-over-the-pcb-board)
    * [10. ボトムプレートにスペーサーをねじ止めする / Attach spacers to the bottom plate with screws](#10-%E3%83%9C%E3%83%88%E3%83%A0%E3%83%97%E3%83%AC%E3%83%BC%E3%83%88%E3%81%AB%E3%82%B9%E3%83%9A%E3%83%BC%E3%82%B5%E3%83%BC%E3%82%92%E3%81%AD%E3%81%98%E6%AD%A2%E3%82%81%E3%81%99%E3%82%8B--attach-spacers-to-the-bottom-plate-with-screws)
    * [11. トッププレートとPCB基板をボトムプレートにはめ込む / Mount the top plate & PCB board over the bottom plate](#11-%E3%83%88%E3%83%83%E3%83%97%E3%83%97%E3%83%AC%E3%83%BC%E3%83%88%E3%81%A8pcb%E5%9F%BA%E6%9D%BF%E3%82%92%E3%83%9C%E3%83%88%E3%83%A0%E3%83%97%E3%83%AC%E3%83%BC%E3%83%88%E3%81%AB%E3%81%AF%E3%82%81%E8%BE%BC%E3%82%80--mount-the-top-plate--pcb-board-over-the-bottom-plate)
    * [12. トッププレートをねじ止めする / Screw the top plate and PCB board to bottom plate](#12-%E3%83%88%E3%83%83%E3%83%97%E3%83%97%E3%83%AC%E3%83%BC%E3%83%88%E3%82%92%E3%81%AD%E3%81%98%E6%AD%A2%E3%82%81%E3%81%99%E3%82%8B--screw-the-top-plate-and-pcb-board-to-bottom-plate)
    * [13. ファームウェアを書き込む / Flash the Firmware](#13-%E3%83%95%E3%82%A1%E3%83%BC%E3%83%A0%E3%82%A6%E3%82%A7%E3%82%A2%E3%82%92%E6%9B%B8%E3%81%8D%E8%BE%BC%E3%82%80--flash-the-firmware)

## 材料 / Parts

| 名前 / Name | 個数 / Qty | 備考 / Remarks | 入手方法 / Where to buy |
| -- | -- | -- | -- |
| トッププレート<br>Top plate | 1 | | TBD: https://github.com/tamano/quali5/tree/add-build-guide/plates |
| PCB基板<br>PCB board | 1 | | TBD: https://github.com/tamano/quali5/tree/add-build-guide/gerber-pcb |
| ボトムプレート<br>Bottom plate | 1 | | TBD: https://github.com/tamano/quali5/tree/add-build-guide/plates |
| ProMicro | 1 | ピンヘッダ付属のもの<br>Choose one includes pin headers | https://shop.yushakobo.jp/products/pro-micro |
| OLED | 1 | ピンヘッダ付属のもの<br>Choose one includes pin headers<br>ピンソケットは不要です<br>Pin Socket is not need | https://shop.yushakobo.jp/products/oled |
| タクタイルスイッチ<br>Tactile switch| 1 | リセットスイッチ用<br>Use as reset switch | https://shop.yushakobo.jp/products/a0800ts-01-1 |
| キーキャップ<br>Keycap | 5 | Kailh Chocロープロファイル互換のもの<br> Choose Kailh Choc V1 compatible one | https://shop.yushakobo.jp/products/pg1350cap-blank |
| キースイッチ<br>Key switch | 5 | Kailh Chocロープロファイル互換のもの<br> Choose Kailh Choc V1 compatible one | https://shop.yushakobo.jp/products/pg1350 |
| スイッチ用PCBソケット<br>PCB Hot-swappable sockets | 5 | Kailh Chocロープロファイル互換のもの<br> Choose Kailh Choc V1 compatible one | https://shop.yushakobo.jp/products/a01ps?variant=37665172553889 |
| 表面実装ダイオード<br>Surface mount diode | 5 | | https://shop.yushakobo.jp/products/a0800di-02-100 |
| M2スリムヘッド小ネジ(5mm)<br>Slim head small screw M2x5 | 5 | ボトムプレート用<br>Use to fix bottom plate | https://shop.yushakobo.jp/products/a0800s2 |
| M2丸型スペーサー(6mm)<br>Round Spacer M2x6 | 5 | | https://shop.yushakobo.jp/products/a0800c2 |
| M2ネジ(3mm)<br>Screw M2x3 | 5 | トッププレート用<br>Use to fix top plate | https://ja.aliexpress.com/item/33022872348.html |

## 組み立て手順
### 1. ダイオードをハンダ付けする / Solder diodes
<img alt="quali5-top" src="https://raw.githubusercontent.com/tamano/quali5/main/img/IMG_2099.jpg" width=480px>

PCBソケットのマークがある面(あるいは、Quali5の名前が書いてない面)にダイオードをハンダ付けします。

その際、ダイオードの向きは、写真のように縦棒のマークが左側に来るように注意してください。

<br>

Solder diodes to the side which have PCB socket marks on it (or the side Quali5 is not printed).

Be careful to orient the diode so that the vertical bar mark is on the left side, as shown in the picture.

<br>

### 2. スイッチ用PCBソケットをハンダ付けする / Solder PCB Hot-swappable sockets
<img alt="quali5-top" src="https://raw.githubusercontent.com/tamano/quali5/main/img/IMG_2103.jpg" width=480px>

PCBソケットのマークに重なるように、スイッチ用PCBソケットをハンダ付けします。

<br>

Solder the PCB Hot-swappable sockets as the marks instructs.

<br>

### 3. ピンヘッダをハンダ付けする / Solder pin headers to PCB plate
<img alt="quali5-top" src="https://raw.githubusercontent.com/tamano/quali5/main/img/IMG_1964.jpg" width=320px> <img alt="quali5-top" src="https://raw.githubusercontent.com/tamano/quali5/main/img/IMG_1963.jpg" width=320px>

ピンヘッダをPCB基板にハンダ付けします。

その後、2枚目の写真のように、裏側の余った足を切り落としてください。ここに出っ張りが残ると、後でトッププレートがPCBから浮いてしまう可能性があります。

<br>

Solder the pin headers to the PCB board.

Then cut off the excess legs on the back side, as shown in the second picture. If there is any protrusion left here, it may cause the top plate does not fit to the PCB board lately.

<br>

### 4. ProMicroをハンダ付けする / Solder the ProMicro
<img alt="quali5-top" src="https://raw.githubusercontent.com/tamano/quali5/main/img/IMG_1965.jpg" width=480px>

ProMicroをUSB差し込み口が外側になる向きで、PCB基板に半田付けします。

ここでも同様に、ハンダ付けの後で余った足を切り落としてください。

<br>

Solder the ProMicro to the PCB board with the USB port facing outward.

After soldering, cut off the excess legs as we did with pin headers.

<br>

### 5. リセットスイッチをハンダ付けする / Solder a reset switch
<img alt="quali5-top" src="https://raw.githubusercontent.com/tamano/quali5/main/img/IMG_1967.jpg" width=480px>

リセットスイッチをPCB基板にハンダ付けします。
<br>

Solder a reset switch to the PCB board.

<br>

### 6. OLEDにピンヘッダをハンダ付けする / Solder a pin header to an OLED
<img alt="quali5-top" src="https://raw.githubusercontent.com/tamano/quali5/main/img/IMG_1968.jpg" width=480px>

OLEDをPCB基板にハンダ付けする準備として、まずはOLEDに付属のピンヘッダをハンダ付けします。

この時、ピンヘッダの向きに注意してください。ピンヘッダは写真のようにディスプレイと反対側から差し込んだ上で、ディスプレイ側の面をハンダ付けします。

<br>

Solder a pin header that come with OLED to it mountable on PCB board.

Be careful to the direction of the pin header. Confirm that insert it from the opposite side of the display and then solder the display side as shown in the picture.

<br>

### 7. OLEDをハンダ付けする / Solder the OLED to the the PCB plate
<img alt="quali5-top" src="https://raw.githubusercontent.com/tamano/quali5/main/img/IMG_1970x.jpg" width=480px>

OLEDをPCB基板にハンダ付けします。

<br>

Solder the OLED to the PCB board.

<br>

### 8. スイッチとキーキャップをトッププレートにはめる / Attach switchs and keycaps to the top plate
<img alt="quali5-top" src="https://raw.githubusercontent.com/tamano/quali5/main/img/IMG_2094.jpg" width=480px>

キーキャップをキースイッチにはめた上で、キースイッチをトッププレートにははめます。

この時点では少しぐらつきますが、心配ありません。

<br>

Put the keycaps on the key switchs, and then put them on the top plate.

It may wobble a little at this point, but don't worry.

<br>

### 9. トッププレートをPCB基板にはめ込む / Mount the top plate over the PCB board
<img alt="quali5-top" src="https://raw.githubusercontent.com/tamano/quali5/main/img/IMG_2093.jpg" width=480px>

トッププレートのキースイッチの足がPCB基板のソケットの位置と合っている事を確認しながら、トッププレートをPCB基板にはめます。

はめるとスイッチがトッププレートから浮きますが、足の位置が合っていれば、上から抑えるとパチンとはまるはずです。

<br>

Fit the top plate to the PCB board , making sure that the legs of the key switchs on the top plate are aligned with the sockets on the board.

The switch will lift off the top plate when you insert it, but if the legs are aligned, it should snap into place when you push it in.

<br>

### 10. ボトムプレートにスペーサーをねじ止めする / Attach spacers to the bottom plate with screws
<img alt="quali5-top" src="https://raw.githubusercontent.com/tamano/quali5/main/img/IMG_2095.jpg" width=480px>

写真の向きにスペーサーをボトムプレートに取り付け、裏側からネジで固定します。

<br>

Attach the spacers to the bottom plate in the orientation shown in the photo, and fix it with screws from the back side.

<br>

### 11. トッププレートとPCB基板をボトムプレートにはめ込む / Mount the top plate & PCB board over the bottom plate
<img alt="quali5-top" src="https://raw.githubusercontent.com/tamano/quali5/main/img/IMG_2097.jpg" width=480px>

トッププレートとPCB基板を、PCB基板の穴がスペーサーにはまるようにボトムプレートに被せます。

<br>

Mount the top plate and PCB board over the bottom plate with the spacers fit into the holes in the PCB board.

<br>

### 12. トッププレートをねじ止めする / Screw the top plate and PCB board to bottom plate
<img alt="quali5-top" src="https://raw.githubusercontent.com/tamano/quali5/main/img/IMG_2098.jpg" width=480px>

トッププレートの上からねじ止めでボトムプレートを固定して完成です。

<br>

Fix the bottom plate by screwing it on top of the top plate and you are done.

<br>

### 13. ファームウェアを書き込む / Flash the Firmware

完成したキーボードをUSBケーブルでPCに接続した上で、以下のコマンドを実行してファームウェアを書き込みます。

まだQMKをインストールしていない場合は、[こちらの手順](https://docs.qmk.fm/#/ja/newbs_getting_started)に従って `2. ビルド環境を準備する` まで実施して環境を整えた上で、以下のコマンドを実施してください)

<br>

Connect the completed keyboard to the PC with a USB cable, and execute the following command to write the firmware.

If you have not installed QMK yet, please follow [this procedure](https://docs.qmk.fm/#/newbs_getting_started) to `2. Prepare Your Build Environment`, and then execute the following command)

<br>

```bash
cd your_workspace_directory
qmk setup tamano/qmk_firmware --branch quali5
cd qmk_firmware
qmk flash -kb tamano/quali5 -km default          # 画面で指示されたらリセットボタンを押す / Push the reset button when instructed
```
