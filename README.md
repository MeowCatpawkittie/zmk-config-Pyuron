#mainブランチ=PMW3610 paw3220ブランチ=PAW3222/PAW3220

#ファームウェア更新手順とキーマップの編集

## ZMK Studioによるキーマップの編集
### 手順1. 有線接続でキーマップを変更する場合は[ZMK Studio](https://zmk.studio/)にアクセス
### 手順2. 中央にある"USB"をクリックしてデバイスを選択することでキーマップの編集が可能になります。
### 手順3. 無線接続でキーマップを変更する場合は[ZMK Studioネイティブアプリ](https://zmk.studio/download)にアクセスしてファイルをダウンロード
### 手順4. インストール後に起動、接続中のデバイスが表示されるのでデバイスを選択するとキーマップの編集が可能になります。

## Keymap-Editorによるキーマップの編集 (Githubアカウントが必要になります)
### 手順1. [Pyuronリポジトリ](https://github.com/MeowCatpawkittie/zmk-config-Pyuron) リポジトリをFork
### 手順2. Actionsタブを選択して"I understand my workflows, go ahead and enable them"をクリック
### 手順3. [Keymap-Editor](https://nickcoutsos.github.io/keymap-editor/)にアクセス
### 手順4. Githubでログインをしたあと"Only select repositories"を選択、"Add Repository"をクリック
### 手順5. 再度"Only select repositories"を選択、"Install"をクリック
### 手順6. キーマップが表示され、編集可能になります。
### 手順7. 編集が完了したら左上の"Save"をクリック、ビルドが完了すると"Latest"からダウンロードできます。
### ダウンロードしたファームウェアは以下の手順で書き込んでください。

## ファームウェアの書き込み

### 手順1. PCと右側ボードを接続します。
### 手順2. 表にあるリセットスイッチ用のボタンを2回素早く押すとブートローダーが起動して"XIAO SENSE"として認識されます。
### 手順3. まずは"XIAO SENSE"ドライブに"settings_reset-seeeduino_xiao_ble-zmk.uf2"を書き込みます。
### 手順4. 次に同じ手順でブートローダーを起動し"Pyuron_R rgbled_adapter-seeeduino_xiao_ble-zmk"を書き込みます。
### 手順5. 右側が終わったら左側も同じように"settings_reset-seeeduino_xiao_ble-zmk.uf2"から"Pyuron_L rgbled_adapter-seeeduino_xiao_ble-zmk"を書き込みます。
### 手順6. 書き込みが完了したら念の為1回リセットボタンを押してください。
### 手順7. 左右どちらも電源をオンにしたあとにBlutoothデバイスの追加から"Pyuron"を選択し、接続ができたらファームウェアの書き込みは完了です。


#### ・ファームウェアの書き込みの際エラーが出ていても実際には正常で書き込めています。手順を進めて問題ありません。
#### ・ファームウェアを更新する際は一度PC側のデバイスから削除して再度ペアリングをしてください。
