# ビルドガイド / Build Guide

## 材料 / Parts

## 組み立て手順
### 1. ダイオードをハンダ付けする / Solder diodes
<img alt="quali5-top" src="https://raw.githubusercontent.com/tamano/quali5/add-build-guide/img/IMG_2099.jpg" width=480px>

### 2. スイッチ用PCBソケットをハンダ付けする / Solder PCB Hot-swappable sockets
<img alt="quali5-top" src="https://raw.githubusercontent.com/tamano/quali5/add-build-guide/img/IMG_2103.jpg" width=480px>

### 3. ピンヘッダをハンダ付けする / Solder pin headers to PCB plate
<img alt="quali5-top" src="https://raw.githubusercontent.com/tamano/quali5/add-build-guide/img/IMG_1964.jpg" width=320px> <img alt="quali5-top" src="https://raw.githubusercontent.com/tamano/quali5/add-build-guide/img/IMG_1963.jpg" width=320px>

ハンダ付けの後、余った足を切る事。

Cut off the excess legs after soldering.

### 4. ProMicroをハンダ付けする / Solder the ProMicro
<img alt="quali5-top" src="https://raw.githubusercontent.com/tamano/quali5/add-build-guide/img/IMG_1965.jpg" width=480px>


### 5. リセットスイッチをハンダ付けする / Solder a reset switch
<img alt="quali5-top" src="https://raw.githubusercontent.com/tamano/quali5/add-build-guide/img/IMG_1967.jpg" width=480px>

### 6. OLEDにピンヘッダをハンダ付けする / Solder a pin header to an OLED
<img alt="quali5-top" src="https://raw.githubusercontent.com/tamano/quali5/add-build-guide/img/IMG_1968.jpg" width=480px>

### 7. OLEDをハンダ付けする / Solder the OLED to the the PCB plate
<img alt="quali5-top" src="https://raw.githubusercontent.com/tamano/quali5/add-build-guide/img/IMG_1970x.jpg" width=480px>

### 8. スイッチとキーキャップをトッププレートにはめる / Attach switchs and keycaps to the top plate
<img alt="quali5-top" src="https://raw.githubusercontent.com/tamano/quali5/add-build-guide/img/IMG_2094.jpg" width=480px>

### 9. トッププレートをPCB基板にはめ込む / Mount the top plate over the PCB board
<img alt="quali5-top" src="https://raw.githubusercontent.com/tamano/quali5/add-build-guide/img/IMG_2093.jpg" width=480px>

### 10. ボトムプレートにスペーサーをねじ止めする / Attach spacers to the bottom plate with screws
<img alt="quali5-top" src="https://raw.githubusercontent.com/tamano/quali5/add-build-guide/img/IMG_2095.jpg" width=480px>

### 11. トッププレートとPCB基板をボトムプレートにはめ込む / Mount the top plate & PCB board over the bottom plate
<img alt="quali5-top" src="https://raw.githubusercontent.com/tamano/quali5/add-build-guide/img/IMG_2097.jpg" width=480px>

### 12. トッププレートをねじ止めする / Screw the top plate and PCB board to bottom plate
<img alt="quali5-top" src="https://raw.githubusercontent.com/tamano/quali5/add-build-guide/img/IMG_2098.jpg" width=480px>

### 13. ファームウェアを書き込む / Flash the Firmware

```bash
cd workspace_directory
qmk setup tamano/qmk_firmware --branch quail5
qmk flash -kb tamano/quali5 -km default          # push reset button when instructed
```