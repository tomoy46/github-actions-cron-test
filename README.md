# github-actions-cron-test

GitHub Actions の `schedule`（cron）動作を確認するためのリポジトリです。

## 確認方法

1. この変更をデフォルトブランチへ反映します。
2. リポジトリの **Actions** タブで **cron動作確認** を開きます。
3. **Run workflow** から手動実行できることを確認します。
4. 5分ごとの schedule 実行を待ち、実行ログに次の情報が表示されることを確認します。
   - 現在のUTC時刻
   - 現在の日本時間
   - `github.event_name`
   - `github.actor`

schedule は UTC 基準の `*/5 * * * *` に設定しています。GitHub Actions の schedule 実行は、混雑状況によって遅れる場合があります。

> [!IMPORTANT]
> 5分ごとの設定は動作テスト用です。テスト完了後は、不要な実行を避けるため、必ず運用で使用する通常時刻の schedule に戻してください。
