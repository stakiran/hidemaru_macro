# 秀丸エディタマクロ
あると便利な秀丸エディタマクロ。

<!-- toc -->
- [秀丸エディタマクロ](#秀丸エディタマクロ)
  - [要件](#要件)
  - [入手](#入手)
  - [使い方](#使い方)
  - [マクロ解説](#マクロ解説)
    - [change_tab_and_title.mac](#change_tab_and_titlemac)
    - [clickable_opener.mac](#clickable_openermac)
    - [commandlist.mac](#commandlistmac)
    - [explorer_pain_autosync.mac](#explorer_pain_autosyncmac)
    - [move_tab_to_left.mac](#move_tab_to_leftmac)
    - [move_tab_to_right.mac](#move_tab_to_rightmac)
    - [open_parent_folder.mac](#open_parent_foldermac)
    - [pathjump.mac](#pathjumpmac)
    - [quicktest_edit.mac](#quicktest_editmac)
    - [quicktest_run.mac](#quicktest_runmac)
    - [smart_filehist.mac](#smart_filehistmac)
  - [License](#license)
  - [Author](#author)

## 要件
以下環境で動作確認済。

- Windows 7 or 10
- 秀丸エディタ V8.69

## 入手
[Download Zip](https://github.com/stakiran/hidemaru_macro/archive/master.zip) より。

## 使い方
- 下記マクロファイルたちをマクロ登録する
- ツールバーにアイコンを配置するなり、キー割り当てで割り当てるなり

各マクロの使い方については下記またはマクロファイル中のコメントを参照。

## マクロ解説

### change_tab_and_title.mac
タブ名とタイトル名を固定する。

### clickable_opener.mac
「ファイル名と思わしき場所、ホームページURL、メールアドレスでカラー表示されている部分」にカーソルがあるとき、それを一発で開く。

内部的には openbyshell 命令を呼び出しているだけ。

### commandlist.mac
「コマンド一覧」を表示する。

内部的には execcommand 命令を呼び出しているだけ。

### explorer_pain_autosync.mac
ファイルマネージャ枠を自動で同期するためにマクロ。

使い方:

- [マクロ] メニュー > [マクロ登録] > 自動起動
- 自動起動マクロを有効にする
- アクティブ切り替え後 にこのマクロをセット

つまりアクティブな秀丸エディタが切り替わる度にこのマクロ（内部的には同期処理をしているだけ）が呼び出されるようにすることで、擬似的に同期を実現。

### move_tab_to_left.mac
今開いているタブを一つ左に動かす。ループする。

### move_tab_to_right.mac
今開いているタブを一つ右に動かす。ループする。

### open_parent_folder.mac
今開いているファイルがあるフォルダを開く。

### pathjump.mac
カーソル位置にあるファイルパスを秀丸エディタで開く。

対応している表記

- filename.ext ← filename.ext を開く
- filename.ext@20 ← filename.ext の 21 行目を開く
- filename.ext#apple ← filename.ext を開いて apple で検索する

### quicktest_edit.mac
quicktest_run.mac を秀丸エディタで開く。

quicktest_run.mac と合わせてツールバーに置いておけば「クリック一発でマクロ編集用ファイルを呼び出す」「クリック一発で実行できる」というお手軽テスト環境がつくれる。

### quicktest_run.mac
quicktest_edit.mac とセットで使う。軽く試したいマクロ内容をここに書く。

### smart_filehist.mac
ファイル名のみを表示する＆キーボードアクセラレータがファイル名先頭文字になっているファイルヒストリ。

## License
[MIT License](LICENSE)

## Author
[stakiran](https://github.com/stakiran)
