# My Calendar Viewer

GitHub Pagesで動作するパーソナルカレンダー。

## 特徴

- ✅ **自動読み込み** - ページを開くと自動的にカレンダーを表示
- ✅ **設定不要で閲覧可能** - URLを埋め込んでおけば誰でも閲覧可能
- 📅 **複数表示モード** - 月/週/日表示切替

## セットアップ

### 1. Google Calendarを公開

1. [Google Calendar](https://calendar.google.com)を開く
2. 左側のカレンダー一覧で対象カレンダーの「⋯」→「設定と共有」をクリック
3. 「アクセス権の設定」で「一般に公開する」をON
4. 「公開用アドレス」のicalリンクをコピー
   - 形式: `https://calendar.google.com/calendar/ical/xxxx/public/basic.ics`

### 2. URLをコードに設定

`index.html`を開いて、以下の部分にURLを貼り付け：

```javascript
// ============================================
// 設定: ここにあなたのGoogle Calendar公開URLを入力
// ============================================
const DEFAULT_CALENDAR_URL = 'https://calendar.google.com/calendar/ical/xxxxx/public/basic.ics';
// ============================================
```

### 3. GitHub Pagesにデプロイ

```bash
git add index.html
git commit -m "Update calendar URL"
git push origin main
```

GitHubリポジトリのSettings → PagesでGitHub Pagesを有効化。

## 使い方

ページを開くだけで自動的にカレンダーが表示されます。

設定を変更したい場合は右上の「設定」ボタンから：
- 🔗 別のURLから読み込み
- 📋 iCalデータを直接貼り付け
- 📁 .icsファイルをアップロード

## 技術スタック

- FullCalendar v6
- ical.js
- Tailwind CSS
- CORS Proxy (allorigins.win)

## 注意事項

- **公開カレンダーのみ対応** - 秘密アドレスは使用しないでください
- カレンダーを非公開にすると表示されなくなります
- CORSプロキシは無料サービスのため、安定性は保証されません

## License

MIT
