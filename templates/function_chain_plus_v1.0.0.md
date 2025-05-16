🔗 Function Calling & 高度連鎖テンプレ集（v1.0.0）

このドキュメントは、GPT Tutor Package v1.0 の連鎖出力とFunction Calling支援を最大化するテンプレート集です。

## 🚀 Slack通知→Notion連携テンプレ

📎 目的：Slackでの問い合わせをトリガーに、Notionに要点を記録

```markdown
【レベル:3】【構成:API仕様】【形式:json】【連鎖:true】【目的:問合対応】
```

🧾 出力例（抜粋）

```json
{
  "functions": [
    {"trigger": "slack_webhook", "url": "/slack/inquiry", "method": "POST"},
    {"action": "create_notion_page", "url": "/notion/log", "method": "POST"}
  ]
}
```

## 🔄 ステップ連鎖テンプレ（例：要件分析→提案→仕様）

📎 目的：構造設計を3段階に分けて自動生成

```markdown
【レベル:3】【構成:構造図】【連鎖:true】【目的:段階的構成支援】
```

🧾 出力構成：

1. ユーザー要件分析 → 2. ソリューション提案 → 3. API構造化

## 🔁 Zapier登録テンプレ（英語・業務連携）

📎 目的：Zapier上でのアクション定義

```markdown
【レベル:3】【構成:API仕様】【形式:json】【トーン:英語】【連鎖:true】【目的:Zapier Automation】
```

🧾 出力：Function Calling形式のJSON構成

---

本テンプレ群は、`--chain true` 指定時に適用される。

最終更新日：2025年5月13日
