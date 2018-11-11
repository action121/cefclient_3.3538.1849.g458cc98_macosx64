# cefclient\_3.3538\.1849\.g458cc98\_macosx64

* cef\_binary\_3\.3538\.1849\.g458cc98\_macosx64\_minimal\.tar\.bz2 (Minimal Distribution) を[http://opensource.spotify.com/cefbuilds/index.html](http://opensource.spotify.com/cefbuilds/index.html) からダウンロードします。   
* ./Release から Chromium Embedded Framework.framework をコピーしてくだい。
* Minmun system version 10.13 に変更して、Deprecated関数を使っている時にエラーが出るのを切ってあります。　   
* ファイルのコピーをRunscriptで行うように変更しました。

<!---->

* Download cef\_binary\_3\.3538\.1849\.g458cc98\_macosx64\_minimal\.tar\.bz2 (Minimal Distribution) from [http://opensource.spotify.com/cefbuilds/index.html](http://opensource.spotify.com/cefbuilds/index.html)       
* Copy Chromium Embedded Framework.framework in ./Release folder.   
* Changed Minmun system version to 10.13 and Deprecated Functions to NO.
* Changed postprocessing to run with Runscript

--

CEF自体をビルドすると私の環境では12時間くらいかかりますので、機能を特に追加しない場合には
[http://opensource.spotify.com/cefbuilds/index.html](http://opensource.spotify.com/cefbuilds/index.html) からビルド済みのFrameworkをダウンロードして使いましょう。   
「Standard Distribution」をダウンロードして、CMakeで解凍したフォルダでConfigureをしてGenerateを行えばXcodeのプロジェクトができます。   
上記手順で作成したXcodeのプロジェクトにはいくつかのサンプルが含まれています。   
このリポジトリにアップしてあるコードは名前の通りcefclient以外のサンプルコードを削除していて雛形として使いやすくなっていいると思います。  
デフォルトだとXcodeのプロジェクトで Minmun system version が10.9なので10.13に変更しました。   
10.13に変更したことでいくつかの関数がDeprecatedになったので、Deprecated FunctionsをNOに変更してあります。