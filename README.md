### ■サービス概要
タイピングとRuby/Railsの学習が１つのサイトでできるRuby/Rails特化の学習サービスです。学習→タイピングを繰り返すことで、知識定着＆タイピング速度UPができます。

### ■ このサービスへの思い・作りたい理由

プログラミング学習中、開発スピードを上げるためタイピング速度をより早くしたいと考えていましたが、知識習得に時間を割くことを優先しがちで、継続してタイピング練習に取り組むことができませんでした。<br>
そのため、知識習得とタイピング練習がまとめてできれば、片方を疎かにせずに継続的に取り組めるかつ楽しく学習できるのではと考えました。

### ■ ユーザー層について
対象ユーザー層：<br>
Ruby/Railsの初学者で、学習しながらタイピング速度を向上させたい方<br>
理由：<br>
①タイピング速度が遅いプログラミング初学者にとって、学習しながらタイピング速度を向上させるサイトがあれば需要があると考えたため<br>
②学習した内容をアウトプットする時に、タイピング練習が同時に行えれば効率的だと考えたため

### ■サービスの利用イメージ
**【利用イメージ】**<br>

学習したい内容（Ruby/Railsに特化）について、タイピングとクイズゲームを通してタイピング速度の向上と理解度チェックを図ります。<br>
また、学習記録を管理でき、ゲーム実績はランキング形式とし、ユーザー同士で実績をシェアできます。<br>
タイピングとクイズゲームについて具体的な内容は以下の通りです。<br>
<u>タイピングゲーム</u><br>
使用頻度の高いメソッド名（ifやmapなど）とそのメソッドで出来ること・使用例をタイピング問題として出題します。以下は一例で、メソッドの説明文や使用例のコードをタイピング問題として出題します。コードをタイピングする場合は、半角スペースや改行もタイピングに含める想定でいます。
```
タイピング問題例１

ifは条件式を評価した結果が真である時、then 以下の式を評価します。 if の条件式が偽であれば elsif の条件を評価します。
```

```
タイピング問題例２

if age >= 12 then
  print "adult fee\n"
else
  print "child fee\n"
end
gender = if foo.gender == "male" then "male" else "female" end
```

<u>クイズゲーム</u><br>
4択のクイズで１つの選択肢を選んで回答するクイズにすることを考えています。クイズ内容のイメージは、RUNTEQの基礎STEP総復習クイズのような理解できていないと初学者が引っ掛かりそうな内容を中心に出題します。また、クイズ結果画面では正解数に加え、クイズの解説を入れる想定です。


**【得られるもの】**
- Ruby/Railsの基礎的な知識
- タイピング速度の向上

### ■ ユーザーの獲得について
Ruby/Railsの初学者でタイピング速度を早くしたいユーザーに対して、学習とタイピング練習を効率的に実施できることをアピールする。

### ■ サービスの差別化ポイント・推しポイント
**【競合するサービス】**<br>
- [Codedrill](https://www.code-drill.com/chars/typing/type_Ruby)：Rubyのタイピングゲーム

**【差別化ポイントと優位点】**<br>
- RubyとRails両方を学習しながらタイピング練習できる点
- タイピングとクイズを併用することで効率的に知識のレベルUP＆タイピング速度UPができる点
- 学習記録を管理できる点
- ゲーム実績をユーザーとシェアできる点

### ■ 機能候補
**【MVPリリース時】**<br>
- ログイン機能
- ゲストログイン機能
- 検索機能
- プロフィール画像投稿機能
- タイピング練習機能
- クイズ機能
- 学習記録管理機能
- ユーザーのCRUD機能
- Xへの投稿機能
- ランキング表示機能
- お気に入り機能

**【本リリース時】**<br>
- タイピング実績のグラフ化
- 管理者画面
- CSVインポート・エクスポート機能


### ■ 機能の実装方針予定
フロントエンドに関しては、過去にチーム開発でReact,Reduxでの開発経験があるため、作成初期から実装したいと考えております。
Typescriptについては、キャッチアップが不十分なためMVPリリース後にキャチアップを予定しています。
#### 使用予定技術一覧
フロントエンド：React、Typescript<br>
  - コード解析 / フォーマッター: ESlint&prettier
  - CSSフレームワーク: Tailwind CSS
  - 状態管理ライブラリ：Redux

バックエンド：Ruby、Ruby on Rails<br>
  - コード解析 / フォーマッター: Rubocop
  - テストフレームワーク: RSpec

データベース：Mysql<br>
インフラ：AWS/Nginx/Unicorn/Mysql<br>
開発環境：Doker/Docker-compose<br>
認証：OAuth 2.0

実装予定の機能については、以下のような技術等を使用する想定です。（CRUD機能で実装できるものは割愛）

- ログイン/ゲストログイン機能<br>
Sorcery, OAuth 2.0
- 検索機能<br>
ransack
- プロフィール画像投稿機能<br>
carrierwave＆mini_magick
- タイピング練習機能<br>
Material Tailwind
- クイズ機能<br>
Material Tailwind
- タイピング実績のグラフ化<br>
chartkick
- 管理者画面<br>
Active Adimin
- CSVインポート・エクスポート機能<br>
 activerecord-import

### 画面遷移図/UI
Figma：<br>
画面遷移図
https://www.figma.com/design/miSHjWP3PXquC20SsSSM3U/%E7%94%BB%E9%9D%A2%E8%A8%AD%E8%A8%88?node-id=8%3A299&t=enpz9Xjdo2IGsoee-1<br>
UI
https://www.figma.com/design/miSHjWP3PXquC20SsSSM3U/%E7%94%BB%E9%9D%A2%E8%A8%AD%E8%A8%88?node-id=26%3A650&t=4ielewCafDRu9tic-1

### ER図
https://drive.google.com/file/d/1Ew8D07elvgoHhhJym4vatf2G1fkBOkG/view?usp=sharing

### 使用画面と機能
| トップページ  | ゲーム選択ページ |
| ------------- | ------------- |
| [![Image from Gyazo](https://i.gyazo.com/1d5fb5ffa014b323bac360dbc3becda4.png)](https://gyazo.com/1d5fb5ffa014b323bac360dbc3becda4)  | [![Image from Gyazo](https://i.gyazo.com/59f5dcc32217f8ad6a46916d981cb5db.png)](https://gyazo.com/59f5dcc32217f8ad6a46916d981cb5db) |
| サービス概要の説明および問題を解くボタンを押すことで、ゲーム選択画面へ遷移する。  | クイズゲームかタイピングゲームを選択できる。ログインなしでもプレイ可能であり、ログインしてプレイした場合は、学習記録として結果が残る。  |

| クイズ一覧ページ  | タイピング一覧ページ |
| ------------- | ------------- |
| [![Image from Gyazo](https://i.gyazo.com/662d7d54c60c980d7cd6c3069125f6de.png)](https://gyazo.com/662d7d54c60c980d7cd6c3069125f6de)  | [![Image from Gyazo](https://i.gyazo.com/55766a63ff28184509f0b5352b971560.png)](https://gyazo.com/55766a63ff28184509f0b5352b971560)  |
| 4クイズにはカテゴリー（Ruby or Rails）、レベルの表示あり  | クイズ同様、カテゴリー（Ruby or Rails）、レベルの表示あり |

| ランキング一覧ページ  | 問題検索ページ |
| ------------- | ------------- |
| [![Image from Gyazo](https://i.gyazo.com/67990ed7cee4d83b722e12d4a66bb4de.gif)](https://gyazo.com/67990ed7cee4d83b722e12d4a66bb4de)  | [![Image from Gyazo](https://i.gyazo.com/220dc5ebb1c60d2e670df356cb1ec03c.gif)](https://gyazo.com/220dc5ebb1c60d2e670df356cb1ec03c)  |
| 会員登録したユーザーのタイピング結果をランキングとして表示。タイプ速度とミスタイプ数からスコアを算出しているため、速くてミスタイプが少ないほどスコアが高くなる。  | タイトル名、カテゴリー、レベルで問題を検索することができる。  |

| クイズゲームページ  | クイズ結果ページ |
| ------------- | ------------- |
| [![Image from Gyazo](https://i.gyazo.com/791411e67eb5c26181ca2c80f5441982.gif)](https://gyazo.com/791411e67eb5c26181ca2c80f5441982)  | [![Image from Gyazo](https://i.gyazo.com/b05adca59b2e262805f783ef08872e8d.gif)](https://gyazo.com/b05adca59b2e262805f783ef08872e8d)  |
| 4択クイズで1つのクイズにつき5問出題される。何問目を解いているか把握できるように、画面上部にステッパーを表示。  | 正解数と各クイズの回答およびユーザー回答を表示。画面下部のボタンより問題一覧画面に遷移する。 |

| タイピングゲームページ  | タイピング結果（モーダル） |
| ------------- | ------------- |
| [![Image from Gyazo](https://i.gyazo.com/f8068a80aa732db63d33f660b7519ef1.gif)](https://gyazo.com/f8068a80aa732db63d33f660b7519ef1)  | [![Image from Gyazo](https://i.gyazo.com/20d8262ea9bdb281aabdc30e9da7635c.gif)](https://gyazo.com/20d8262ea9bdb281aabdc30e9da7635c) |
| 1つのタイピング問題につき5問出題される。入力対象文字の場合：背景色グレー＋黒字、正しい入力の場合：緑字、誤入力：赤字で表示。  | タイピング結果をモーダルで表示。表示内容は、タイピング速度、ミスタイプ回数、スコアの3項目。  |

| X投稿機能  | 学習記録ページ |
| ------------- | ------------- |
| [![Image from Gyazo](https://i.gyazo.com/063c1a52f0794c0decff5daa90e3707d.gif)](https://gyazo.com/063c1a52f0794c0decff5daa90e3707d)  | [![Image from Gyazo](https://i.gyazo.com/ded702c30283a361dbe5cd19b1f2de55.gif)](https://gyazo.com/ded702c30283a361dbe5cd19b1f2de55)  |
| タイピング結果を容易にXでシェアできるように投稿ボタンを設置。ボタンを押下後、Xの投稿内容にタイピング結果とアプリのリンク先をあらかじめ表示する。  | ログイン状態でクイズorタイピング問題を解くことで、カレンダーに解いた問題数の実績を表示する。また、タイピングの場合はグラフで過去実績のトレンドを把握することができる。  |

| お気に入り機能  | マイページ |
| ------------- | ------------- |
| [![Image from Gyazo](https://i.gyazo.com/e159de411861af94ca1dcf6743b5cd81.gif)](https://gyazo.com/e159de411861af94ca1dcf6743b5cd81)  | [![Image from Gyazo](https://i.gyazo.com/67b589d4d28d56b853483d316ffa214f.gif)](https://gyazo.com/67b589d4d28d56b853483d316ffa214f)  |
| ログイン状態の場合、各クイズ問題にお気に入りボタンが表示される。お気に入りした問題については、ヘッダー上部のお気に入り一覧から画面遷移することで、容易に問題にアクセスすることができる。  | ログイン状態の場合、ユーザー情報を表示するマイページに遷移することができる。ニックネームやユーザーアイコンの編集などができる。  |
