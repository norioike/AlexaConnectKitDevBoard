# AlexaConnectKit Dev-Boardについて
この基板は主にAlexa Connect Kitを使ったデバイスを開発するための開発ボードとして作りました。
RP2040をMCUにAlexaConnectKitのモジュール "ESP32-PICO-V3-ZERO"と通信ができるようになっています。
またRP2040のGPIOは出せるだけ出しているので、センサー類を追加したり駆動系を追加する事でオリジナルのAlexa対応ロボットなどが作れるようになる（と思います)

ただ、この基板単体でも遊べるようにタクトスイッチとフルカラーLEDを実装しています。
しかし、私のミスでフルカラーLEDは点灯しません。電源は5Vにもかかわらず、3.3Vを供給。そのため命令を送っても点灯しません。

部品が余ったので数個だけ頒布しています。
もしよろしければこちらをご覧下さい。

https://www.switch-science.com/catalog/8078/


## Alexa Connect Kitについて
ハードウェアにAlexaを簡単に統合できるようにするためのマネージメントサービスで、これを使うことでAlexaに話しかけるとハードウェアを動かしたり、
逆にセンサー情報をAlexaに送る事ができるハードウェアを簡単に開発する事ができるようになります。
具体的にAlexa内蔵の電子レンジみたいなものを作ることも可能です。

システムの構成は、従来ハードウェアにAlexaと通信ができるモジュールを搭載することで実現できるようになっています。こうすることで開発負荷を下げることを想定しているのだと思います。
今回はESP32-PICO-V3-ZEROがそのモジュールで、この中にAlexaと通信するために必要なファームウェアが書かれており、開発者がこのモジュールとUARTなどで通信できるようにハードウェアを開発すればOKです。
すべての制御は自身が実装したMCUに書くことになります。ここでAlexaに対して命令を送ったり、受け取ったりできるようにすることでAlexa対応のオリジナルデバイスが実現できます。

## セットアップについて
セットアップはWikiにまとめています。このセットアップが完了できれば、あとは自由に開発するだけの状態になります。
