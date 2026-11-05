i☆Ris Song Search - iPhone用スターター

ファイル:
- index.html : 検索画面
- songs.json : データ（最初は空）

このひな形はindex.htmlとsongs.jsonを同じフォルダに置き、Webサーバー経由で開く想定です。
iPhoneの「ファイル」アプリからHTMLを直接開くと、ブラウザ制限でJSONを読み込めない場合があります。

songs.jsonの登録形式:
{
  "songs": [{"song_id":"S0001","song_title":"曲名","song_title_kana":""}],
  "creators": [{"creator_id":"C0001","creator_name":"作家名"}],
  "credits": [{"credit_id":"CR001","song_id":"S0001","creator_id":"C0001","role":"作詞"}],
  "releases": [], "release_tracks": [], "sources": []
}

roleは「作詞」「作曲」「編曲」。
共作の場合はcreditsに担当者ごとに1行追加します。
同じ曲が複数作品に収録されてもsongsに重複登録せず、release_tracksで管理します。

iPhoneのみでの公開例:
1. GitHubアカウントを作成し、Safariでgithub.comを開く。
2. 新しいrepository（リポジトリ）を作成する。
3. index.htmlとsongs.jsonを同じリポジトリの直下にアップロードする。
4. Repository Settings > Pages から公開元を設定する。
5. 発行されたURLをSafariで開く。

GitHub Pagesはアプリ作成サービスではなく、静的ファイルを公開するホスティング機能です。
公開設定の画面名・利用条件は変更されることがあります。
実際のクレジットは公式情報で確認し、出典も記録してください。
