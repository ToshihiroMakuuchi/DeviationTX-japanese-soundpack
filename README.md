# DeviationTX Japanese Soundpack
## はじめに (Introduction)

まっく@Betaflight日本語化プロジェクトです。日本語化プロジェクトの派生として以前にOpenTX周りの音源を日本語化してみましたが、T8SG V2 Plusの技適OK祭りの勢いもあって？DeviationTX日本語サウンドパックを作成してみました。引き続きDeviation側でも皆様に利用して頂きまして、色々と使い勝手を良くしていければと考えます。



## 説明 (Description)

このリポジトリは、DeviationTX 日本語サウンドパックを提供しています。今回、音源の日本語化にはMicrosoft合成音声エンジン(Ayumi)を用いてテキスト読み上げを行いました。数値読み上げの部分や一部システムメッセージや効果音はフリー素材を用いて組み合わせています。動作確認環境としてはJumper T8SG V2 Plus、またDeviationバージョンはナイトリービルド2019/02/11版を中心に行っております。

このサウンドパックが提供するメッセージフレーズは、下記カテゴリのいずれかに分類されます：

 * DeviationTXシステムメッセージ (System messages) [global]
 * マルチローター関連用語 (Multirotor related) [custom]
 * フリー素材による数値読み上げ、およびシステムメッセージ [anime]
 * フリー素材によるシステム効果音 [system]



## ダウンロードとインストール (Download & Install)

release (https://github.com/ToshihiroMakuuchi/DebiationTX-japanese-soundpack/releases) ページへ移動し、最新のZIPアーカイブファイルをダウンロード、および解凍してください。またご自身の送信機で使用している対象音源を削除します。音源はSDカード内の `mp3 /`以下のディレクトリに収められます。ダウンロードおよび解凍したZIPアーカイブの内容をコピーし、SDカードの `mp3 /`ディレクトリへコピーを行います。

また、ZIPファイルを解凍した際、直下に【voice.ini】ファイルがありますが、これは送信機本体側のDeviationディレクトリ`media /`以下に保存してください。
2019年3月現在、DeviationTXナイトリービルド版は、256ファイル以上の音源ファイルを正常に認識することができません。その為必要とする音源ファイルを150～200程度選定し、ご利用ください。

Deviation送信機では音源対応(Voice Support)を行う場合、ハードウェア自身への音源ユニット(DFPlayer miniもしくは互換ユニット)の追加、また【hartdware.ini】の編集を行う必要があります。詳しくは下記内容をご確認ください。

https://www.deviationtx.com/wiki/voiceoutput



## これらの詳細について (Technical Details)

`index.csv`ファイルは、音源に含まれるすべてのメッセージフレーズのデータベースとなります。
`tools /`ディレクトリにあるPythonスクリプトは、テキスト読み上げをを行いWAVデータを生成するために使用しますが、今回この音源はスクリプトを使用せず別ツールを用いてWAVファイルを生成、もしくはフリー素材音源を加工して生成しています。またCSVファイルは、下記の項目に分かれています。

index.csv項目は【Siri Multirotor Soundpack for OpenTX】に準拠しますが、Deviationにて利用する為、下記内容にて項目を利用しています。

 * `_idx` この項目はvoice.ini内の音源再生長(ms)として利用
 * `_category` 対象メッセージに割り当てられた旧カテゴリ(未使用)
 * `category` 対象メッセージに割り当てられたカテゴリ
 * `directory` 対象メッセージを格納するファイルシステムのパス
 * `_filename`  この項目はvoice.ini内のコメントとして利用
 * `filename` 対象メッセージのファイル名
 * `_text` メッセージフレーズ内容



## フリー素材の使用

合成音声では聴き辛い部分の数値の読み上げに関しては、フリー素材サイト【効果音ラボ】さまのものを、余白音声部分のカットや数値読み上げ合成の編集し、合わせてvoice.iniを作成致しました。配布セットとしてvoice.iniならびに音源を合わせております為、利用にあたりMP3音声ファイル単独での利用は行わないでください。また、単独で調整を行いたい場合には改めて下記サイトより必要なファイルをダウンロードしてご利用ください。

https://soundeffect-lab.info/sound/voice/



## クレジット (Credits)

これらのサウンドパックはPhaeilo氏が提供する【Siri Multirotor Soundpack for OpenTX】をforkし、それをOpenTX用に日本語化したものをDeviationTXでも使用ができるように必要なファイル群をまとめ、合わせてvoice.iniファイルを用意しました。dale3h氏およびPhaeilo氏の、非常にすばらしい英語版サウンドパックの提供に感謝致します。

* Inspiration: "Amber" sound pack by Arron Bates (theKM)
* Original "taranis-siri-sound-pack" by: Dale Higgs (dale3h)
* Improved by: Philip Huppert (Phaeilo)
* Japanese Transration by: まっく (ToshihiroMakuuchi)



## Siri Multirotor Soundpack for OpenTX

fork元であるOpenTX英語版サウンドパックはこちらです。

https://github.com/Phaeilo/opentx-siri-multirotor

## DeviationTX Voice_packs
また、DeviationTXの英語、フランス語、ドイツ語の各種サウンドパックはこちらをご参考としてください。

https://www.deviationtx.com/downloads-new/category/1010-moeder-voice-packs


