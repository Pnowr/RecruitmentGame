# Discord ゲーム募集ボット
<p align="center">
  <img src="1e386160923f3f11377f11688d93141e.png" alt="画像の説明" width="200" />
</p>
<p align="center">
    <a href="https://x.com/intent/follow?screen_name=nau_neko" target="_blank">
        <img src="https://img.shields.io/twitter/follow/nau_neko?logo=X&color=%20%23f5f5f5" alt="follow on X(Twitter)">
    </a>
    <a href="https://www.twitch.tv/nau_neko">
       <img alt="Twitch Status" src="https://img.shields.io/twitch/status/nau_neko">
</p>

日本のDiscordサーバー向けの多機能ゲーム募集管理ボットです。このボットを使用すると、ユーザーは募集投稿を作成し、セッションに参加し、自動通知機能付きで参加者を管理することができます。



## 機能

- **簡単なゲーム募集**: ユーザーはシンプルなUIで募集投稿を作成できます
- **カスタマイズ可能な設定**: 最大プレイヤー数、開始時間、締切時間を設定できます
- **自動通知**: 募集が満員になったり失敗したりした場合にユーザーに通知します
- **ロールメンション**: 募集ロールをメンションして興味のあるプレイヤーに通知します
- **自動クリーンアップ**: ゲーム開始から5分後に募集メッセージを自動的に削除します

## コマンド

- `!setup` - 管理者専用コマンドで、募集ボタンインターフェースをセットアップします

## 仕組み

1. 管理者が `!setup` を使用して募集インターフェースをセットアップします
2. ユーザーは「募集を作成」をクリックし、フォームに記入します：
   - ゲームの説明
   - 最大プレイヤー数
   - ゲーム開始時間
   - 募集締切時間
3. ボットは参加/キャンセルボタン付きの募集を投稿します
4. ユーザーは締切または最大プレイヤー数に達するまで参加または退出できます
5. 募集状況に基づいて自動通知が送信されます
6. ゲーム開始後にメッセージは自動的にクリーンアップされます

## セットアップ手順

1. このリポジトリをクローンします
2. 必要なライブラリをインストールします：
   ```
   pip install discord.py
   ```
3. ボットを設定します：
   - `RECRUITMENT_ROLE_ID` をサーバーの募集ロールIDに置き換えます
   - `TOKEN` 変数にボットトークンを追加します
4. ボットを実行します：
   ```
   python bot.py
   ```

## 設定

スクリプト内で以下の変数を設定する必要があります：

- `RECRUITMENT_ROLE_ID`: 募集投稿でメンションするロールのID
- `TOKEN`: DiscordボットのトークンIU

## 必要条件

- Python 3.8以上
- discord.py 2.0以上
- Discordインテント: message_content, members

## ライセンス

MIT

## 貢献

貢献は歓迎します！お気軽にプルリクエストを提出してください。
