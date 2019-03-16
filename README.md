# DeviationTX Japanese Soundpack
## はじめに (Introduction)

まっく@Betaflight日本語化プロジェクトです。日本語化プロジェクトの派生としてOpenTX周りの音源を日本語化してみましたが、引き続きDeviationTX日本語サウンドパックを作成してみました。引き続きDeviation側でも皆様に利用して頂きまして、色々と使い勝手を良くしていければと考えます。



## 説明 (Description)

このリポジトリは、DeviationTX 日本語サウンドパックを提供しています。今回、音源の日本語化にはMicrosoft合成音声エンジン(Ayumi)を用いてテキスト読み上げを行いました。動作確認環境としてはJumper T8SG V2 Plus、またDeviationバージョンはナイトリービルド2019/02/11版を中心に行っております。

このサウンドパックが提供するメッセージフレーズは、下記カテゴリのいずれかに分類されます：

 * DeviationTXシステムメッセージ (System messages)
 * マルチローター関連用語 (Multirotor related)



## ダウンロードとインストール (Download & Install)

release (https://github.com/ToshihiroMakuuchi/deviationtx-japanese-soundpack/releases) ページへ移動し、最新のZIPアーカイブファイルをダウンロード、および解凍してください。また、ご自身の送信機で使用している対象音源を削除してください。音源はSDカード内の `MP3 /`以下のディレクトリに収められます。ダウンロードおよび解凍したZIPアーカイブの内容をコピーし、SDカードの `MP3 /`ディレクトリへコピーを行います。

また、ZIPファイルを解凍した中に【voice.ini】ファイルがありますが、これは送信機本体側のDeviationディレクトリ`media /`以下に保存してください。
2019年3月現在、DeviationTXナイトリービルド版は、256ファイル以上の音源ファイルを正常に認識することができません。その為必要とする音源ファイルを選択してご利用ください。



## これらの詳細について (Technical Details)

`index.csv`ファイルは、音源に含まれるすべてのメッセージフレーズのデータベースとなります。
`tools /`ディレクトリにあるPythonスクリプトは、テキスト読み上げをを行いWAVデータを生成するために使用しますが、今回この音源はスクリプトを使用せず別ツールを用いてWAVファイルを生成、もしくはフリー素材音源を加工して生成しています。またCSVファイルは、下記の項目に分かれています。

 * `_idx` 対象メッセージが最初に抽出されたファイル名
 * `_category` 対象メッセージに割り当てられた旧カテゴリ
 * `category` 対象メッセージに割り当てられた新カテゴリ
 * `directory` 対象メッセージを格納するファイルシステムのパス
 * `_filename`  対象メッセージの旧ファイル名
 * `filename` 対象メッセージの新ファイル名
 * `_text` メッセージフレーズ内容



## クレジット (Credits)

これらのサウンドパックはPhaeilo氏が提供する【Siri Multirotor Soundpack for OpenTX】をforkし、それを日本語化したものをDeviationTXで使用できるようにvoice.iniファイルを用意しました。dale3h氏およびPhaeilo氏の、非常にすばらしい英語版サウンドパックの提供に感謝致します。

* Inspiration: "Amber" sound pack by Arron Bates (theKM)
* Original "taranis-siri-sound-pack" by: Dale Higgs (dale3h)
* Improved by: Philip Huppert (Phaeilo)
* Japanese Transration by: まっく (ToshihiroMakuuchi)



## Siri Multirotor Soundpack for OpenTX

fork元である英語版サウンドパックはこちらです。

https://github.com/Phaeilo/opentx-siri-multirotor


