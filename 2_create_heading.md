# Ruby on Railsの基礎


## 0.このテキストのゴール
本格的にRuby on RailsでWebアプリケーションを作成するに当たって必要な２つの知識とRuby on Railsのインストールを実践しましょう。

このテキストのゴールは以下の４つとなります。

１．Ruby on Railsを理解する上で必要になるフレームワークとは何かを理解する。

２．Ruby on RailsとMVCフレームワークとは何かを理解する。

３．Ruby on Railsをインストールする。

４．Ruby on Railsのバージョンを確認し、動作を確認する。


## 1.Webアプリケーションとフレームワーク

1-1Webアプリケーションを作成するにはさまざまな知識が必要で、高度な知識が要求されます。<br>
　Webアプリケーションと言ってもクライアント側での処理、サーバー側での処理があり、<br>
　データを記録し、処理をさせるならば、データベースの知識も要求されます。<br>
　これを一から習得、作成するには、大変な労力と高度な知識を伴います。<br>
　それがRuby on Railsの登場により、状況が変化しました。<br>
<br>
　Webアプリケーションを作る際の時間を大幅に短縮し、実際に動作するWebアプリケーションを作れてしまうものです。<br>
<br>
　Ruby on Railsで実際にWebアプリケーションを作成する前にフレームワークとは何かをまず理解しておきましょう。<br>
<br>

## 2.フレームワークとは何か
　フレームワークとは訳すと枠組みと言う単語ですが、あまり馴染みがない単語ですね。<br>
　実生活におけるフレームワークと似たものを想像してみます。<br>
<br>
　皆さんはお料理キットをご存知でしょうか？<br>
<br>
　お料理キットにも種類はありますが、総じて具材があらかじめ、人数分用意されており、カットや皮むきなど<br>
　下ごしらえも済んで、袋ごとにパックされており、付属の手順（レシピ）に沿って、<br>
　手持ちのフライパンや鍋で調理することで、一品が完成するというものです。<br>
<br>
　お料理キットは調理にかかる時間を短縮するばかりでなく、調理の敷居を下げて、簡単な調理だけで、<br>
　完成するために考えられたものです。<br>
　つまり、一品を調理するために必要な要素(具材、カット、味付け、調理の手順等)が<br>
　あらかじめ用意されているのがお料理キットです。<br>
<br>
　プログラミングにおけるフレームワークもこのお料理キットに"類似"しています。<br>
　プログラムの処理の構造や仕組みはおおよそ共通点が多いのですが、この共通部分が動作するように<br>
　あらかじめ用意されており、共通部分以外の固有の部分については、足りない部分を作成者が補うことで<br>
　システムが組めてしまうものです。<br>
<br>
　一からコーディングしなくてもフレームワークが提供するルール（手順）と機能に従って、<br>
　共通以外の固有の部分をコーディングするだけで、動くシステムが組めてしまうという画期的なものです。<br>
　
　
## 3.Ruby on Railsとは何か
　Ruby on Railsとは、Webアプリケーションを作成するためのフレームワークです。<br>
　使いこなすためには、覚えることも多いのですが、多岐に渡るWebアプリケーションを作るための技術の習得と<br>
　機能を一からコーディングするような労力は必要がなく、Webアプリケーション作れてしまう特徴があります。<br>
<br>
　どうやってそれを実現するのかというと次のMVCという内部の処理構造(仕組み)を用いて実現する<br>
　フレームワークとなります。<br>
　次の章で確認してみましょう。<br>
　
## 4.MVCフレームワークとは
　Ruby on Railsを使う上で必要になる知識として、MVCがあります。<br>
　MVCとは何かというと、Ruby on Railsの内部構造を説明する用語で、以下の３つの仕組みの頭文字をとったものです。<br>
<br>
　・Model：データベースにアクセスして、必要なデータをやりとりする機能を提供するもの。<br>
<br>
　・View：テンプレートを使い、プログラムで制御できるようなWebページ（画面）を作成する。<br>
<br>
　・Controller：Webブラウザがアクセスから、ModelやViewを呼び出して、処理し、結果をWebブラウザに<br>
　　　　　　　　返す、一連のプログラムを制御する。<br>
<br>
　プログラム全体を上記３つの要素として、整理して、システムを組むことで一通りのWebアプリケーションが<br>
　組めて仕組みなのです。<br>
　この用語はRuby on Railsで開発を行う上でよく出てくる用語になりますので、<br>
　ざっくりでも良いので覚えておきましょう。<br>
<br>
### 5.Ruby on Railsをインストールしてみよう
　　ここからはRuby2.3.3がインストールされているWindows環境を前提にRuby on Railsを使うための手順を説明します。<br>
<br>
### 5-1.Development Kitをダウンロードする
　　https://rubyinstaller.org/downloads/　　にアクセスします。<br>
<br>
　　ページ下部のDEVELOPMENT KIT (OLD)の箇所で利用しているPCによって、32ビット版、64ビット版のいずれかを<br>
　　ダウンロードします。<br>
　　※お使いのWindowsOSが32ビット版、64ビット版の確認方法は以下の【32ビットと64ビットの確認方法】を<br>
　　参照します。<br>
<br>
　　・Windowsが32ビット版は以下をダウンロードします。<br>
　　　For use with Ruby 2.0 to 2.3 (32bits version only):<br>
　　　　DevKit-mingw64-32-4.7.2-20130224-1151-sfx.exe<br>
<br>
　　・Windowsが64ビット版は以下をダウンロードします。<br>
　　　For use with Ruby 2.0 to 2.3 (x64 - 64bits only)<br>
<br>
　　　　DevKit-mingw64-64-4.7.2-20130224-1432-sfx.exe<br>
<br>
<br>
　　　　【32ビットと64ビットの確認方法】<br>
<br>
　　　◆Windows10の場合<br>
　　　スタートボタンを右クリックし、表示されたメニューのシステムをクリックします。<br>
　　　設定ウィンドウが表示され、右側の中央からやや下のデバイスの仕様に書かれている「システムの種類」に箇所が<br>
　　　32ビットオペレーティングシステムと記載されていたら、32ビット版をダウンロードします。<br>
　　　64ビットオペレーティングシステムと記載されていたら、64ビット版をダウンロードします。<br>
<br>
<br>
　　　◆Windows7の場合<br>
　　　スタートボタンをクリックし、表示されたメニューのコンピュータを右クリックします。<br>
　　　表示されたコントロールパネルのシステムウィンドウでウィンドウ下部の「システムの種類」に<br>
　　　32ビットオペレーティングシステムと記載されていたら、32ビット版をダウンロードします。<br>
　　　64ビットオペレーティングシステムと記載されていたら、64ビット版をダウンロードします。<br>
<br>
<br>
　　次にRubyがインストールされているフォルダを開きます。<br>
　　規定ではC:\Ruby23-x64フォルダ(32ビット版はC:\Ruby23)にインストールされていますので、<br>
　　エクスプローラーを開き、Cドライブをダブルクリックし、Ruby23-x64(32ビット版はC:\Ruby23)フォルダを開きます。<br>
　　フォルダを開いたら、エクスプローラーの右側部分で右クリックし、新規作成→フォルダーをクリックします。<br>
　　新規のフォルダーが作成されるので、フォルダ名をdevkitというフォルダ名称を付けます。<br>
<br>
　　次にダウンロードしてきたDevelopment Kitを作成したdevkitフォルダにコピーします。<br>
　　コピー出来たら、Development Kitをダブルクリックします。<br>
　　展開先が表示されますが、規定のままで進みます。<br>
　　devkitフォルダにevelopment Kitが解凍されます。<br>
<br>
　　次にコマンドプロンプトを起動し、以下のコマンドを入力し、Enterキーを押下します。<br>
　　このコマンドはカレントディレクトリを先程、作成したdevkitフォルダに移動するコマンドです。<br>
<br>
<br>
　　【32ビット版の場合】<br>
　　C:\>cd C:\Ruby23\devkit<br>
　　　↓<br>
　　実行後<br>
　　C:\Ruby23\devkit><br>
<br>
　　【64ビット版の場合】<br>
　　C:\>cd C:\Ruby23-x64\devkit<br>
　　　↓<br>
　　実行後<br>
　　C:\Ruby23-x64\devkit><br>
<br>
<br>
　　次に以下のコマンドを入力し、Enterキーを押下します。<br>
　　c:\Ruby22-x64\devkit>ruby dk.rb init<br>
　　　↓<br>
　　実行後<br>
　　c:\Ruby22-x64\devkit>ruby dk.rb init<br>
　　[INFO] found RubyInstaller v2.3.3 at C:/Ruby23-x64<br>
　　Initialization complete! Please review and modify the auto-generated'<br>
　　config.yml' file to ensure it contains the root directories to all<br>
　　of the installed Rubies you want enhanced by the DevKit.<br>
<br>
<br>
　　次に以下のコマンドを入力し、Enterキーを押下します。<br>
　　c:\Ruby22-x64\devkit>ruby dk.rb install<br>
　　　↓<br>
　　実行後<br>
　　c:\Ruby22-x64\devkit>ruby dk.rb install<br>
　　[INFO] Updating convenience notice gem override for 'C:/Ruby23-x64'<br>
　　[INFO] Installing 'C:/Ruby23-x64/lib/ruby/site_ruby/devkit.rb'<br>
<br>
<br>
　　コマンドプロンプトはそのまま閉じないようにします。次の5-2へ進みましょう。<br>
<br>
### 5-2.Ruby on Rails 5をインストール
　　Ruby on RailsをインストールするにはRubyに付属されているgemと言われるプログラムを使用します。<br>
　　このプログラムはRubyの追加機能をパッケージという単位で管理するプログラムでパッケージマネージャー<br>
　　と呼ばれているプログラムとなります。<br>
　　このgemを使うと必要な機能を追加できるようになっています。<br>
<br>
　　実際にRuby on Railsをgemを使ってインストールします。以下のコマンドを入力し、Enterキーを押下します。<br>
<br>
　　c:\Ruby22-x64\devkit>gem install rails<br>
<br>
　　多くのパッケージがダウンロードされますので、完了するまで数分待ちましょう。<br>
<br>
　　Installing ri documentation for rails-5.2.2<br>
　　Done installing documentation for concurrent-ruby, i18n, thread_safe,<br>
　　tzinfo, activesupport, rack, rack-test, mini_portile2, nokogiri, crass,<br>
　　loofah, rails-html-sanitizer, rails-dom-testing, builder, erubi, actionview,<br>
　　actionpack, activemodel, arel, activerecord, globalid, activejob, mini_mime,<br>
　　mail, actionmailer, nio4r, websocket-extensions, websocket-driver, actioncable,<br>
　　mimemagic, marcel, activestorage, thor, method_source, railties, bundler, sprockets,<br>
　　sprockets-rails, rails after 155 seconds<br>
　　39 gems installed<br>
<br>
　　一番最後に上記のようなメッセージが表示されたら、完了です。<br>
<br>
　　そのままコマンドプロンプトは閉じずに、次で5-3.Ruby on Railsのバージョン確認を実行します。<br>
<br>
### 5-3.Ruby on Railsのバージョンを確認してみよう　　
　　Ruby on Railsがインストールできたら、以下のコマンドを入力してみましょう。<br>
<br>
　　C:\>rails -v<br>
　　Rails 5.2.2<br>
<br>
　　バージョンが表示されることを確認してください。<br>
　　これでRuby on Railsのインストールが完了しました。これからRuby on Railsを使って開発する準備が整いました。<br>
<br>
　　お疲れ様でした。ここまで本テキストは終了です。<br>
<br>
