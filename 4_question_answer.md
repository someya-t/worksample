Railsにおける、「単数」と「複数」の使い分けについての説明です。

例えばコントローラー作成時は"blogs"と、モデル作成時は"blog”
とそれぞれパラメーター指定させています。それに基づいて様々な変数等が自動的に作成されているようなので、
"blogs"と"blog"を使い分けることに意味があるのだと思うのですが、何処にも記載が無いので未だに混乱しています。

rake routes"を行ってみても、Prefixに"blog"　”new_blog"もあれば、"blogs" "confirm_blogs"もあります。
何故こうなっているのか全く理解できていません。



【回答】
Ruby on Railsの命名規則は「複数で扱うもの」が複数形、「単数で扱うもの」が単数形で命名します。
コントローラー、テーブルはすべてのモデルを1つのコントローラー、テーブルで扱うので、複数形で命名します。
モデル作成時は1レコードだけのモデルができるようするため、1レコード単位で扱うことになるので、単数形で命名します。
ですから、コントローラー作成時は"blogs"と命名し、モデル作成時は"blog”を命名して使い分けします。
