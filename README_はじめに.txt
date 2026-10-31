# COCO 初期版

## できること
- Googleログイン
- 家族データの作成
- 予定、タスク、子ども、買い物、家計・投資、物件、仕事、メモの登録・削除
- iPhone向け画面、ホーム画面追加用manifest

## 重要
この版は初期動作版です。AIによる自動判断、OCR、プッシュ通知、写真クラウド保存、家族招待の安全な受け入れ処理はまだ実装していません。
家族IDをコピーする表示はありますが、他のユーザーを安全に家族へ追加する招待フローは未実装です。現状ではGoogleログインした最初のユーザーが家族を作成します。

## 公開手順
1. GitHubで新しいPublicリポジトリを作る（無料）。
2. index.html と manifest.json をルートにアップロード。
3. Settings → Pages → Deploy from a branch → main / root → Save。
4. 表示されたURLをiPhone Safariで開く。
5. Firebase Console → Authentication → Settings → Authorized domains に公開ドメインを追加。
6. Firebase Console → Firestore → Rules に firestore.rules の内容を貼り付けて公開。

## 注意
- FirebaseはSpark無料プランのまま利用してください。Blazeへアップグレードしないでください。
- Firestore無料枠を超えた場合に課金が発生しないよう、Sparkプランを維持してください。
- 本番運用前に招待フローとセキュリティルールを追加テストしてください。
