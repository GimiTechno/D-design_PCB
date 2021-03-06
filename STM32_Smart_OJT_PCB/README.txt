【概要】
株式会社D-design 様の新人研修用基板ソースコード
----------------------------------------------------------------------
【基板スペック】
本基板は下記をフォークし専用に開発した基板です。

Open H/W 『STM32　Smart』
URL：https://stm32-base.org/boards/STM32F103C8T6-STM32-Smart-V2.0.html
----------------------------------------------------------------------
マイコン ... STマイクロ STM32F103C8T6
(https://www.stmcu.jp/stm32/stm32f1/stm32f103/12022)
クリスタル ... 8MHz
クロック　…　72MHz
ROM ... 64KB
RAM ... 20KB
----------------------------------------------------------------------
【開発環境】
下記2つを用意してください。

・STM32CubeIDE
URL＠　https://www.st.com/ja/development-tools/stm32cubeide.html

・TeraTerm
URL＠　https://ja.osdn.net/projects/ttssh2/
----------------------------------------------------------------------
【サンプルアプリ】
SRCフォルダのソースはサンプルアプリ

『サンプルアプリ動作』
****************************************************
① 電源を投入し、TeraTermを開くと
下記オープニングメッセージが表示される

"STM32 DevelopmentBoard SampleApp
Ver1.0(2020.12.21 Build)
Copyright 2020 D-design.,Co.Ltd."

② ユーザボタンを押すたび
⇒　"USR_BTN was ON ... LED Toggle"がVCP経由で表示される。
****************************************************
『サンプルアプリの改造』
① サンプルアプリのSTM32CubeIDEのプロジェクトファイルをダブルクリック
② Core\Src\main.cのメイン関数でアプリを載せていくのみ

『サンプルアプリの仕組み概要』
① ドライバでUSBのVCP（仮想COMポート）が動いているのでUARTのように文字が表示される
② ボタンは外部割込みで処理している
※チャタリングの心配不要
----------------------------------------------------------------------
以上