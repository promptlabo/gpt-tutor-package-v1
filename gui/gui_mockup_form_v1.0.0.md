🖥 GPT Tutor Package GUIフォーム構成案（v1.0.0）

このドキュメントは、Notion/Figma等でのGUI入力フォームに適用できる「入力→CLI構文変換対応」UIモック案を記述したものです。

---

## 📋 入力フィールド定義

| ラベル     | 型                            | CLI変換例                     |
| ------- | ---------------------------- | -------------------------- |
| 出力レベル   | セレクト（1/2/3）                  | `--level 2`                |
| 出力構成    | セレクト（構造図／LP／API仕様／教材など）      | `--structure LP`           |
| トーン     | セレクト（カジュアル／ビジネス／英語）          | `--tone business`          |
| 出力形式    | セレクト（markdown/json/text）     | `--format markdown`        |
| セクション選択 | チェックボックス（summary〜reflection） | `--section summary+prompt` |
| 連鎖出力    | トグルスイッチ（ON/OFF）              | `--chain true`             |
| 職種・属性   | テキスト入力                       | `--persona 開発者`            |
| 目的・用途   | テキスト入力                       | `--purpose 提案書作成`          |

---

## 🧪 出力例（CLI変換）

入力：

* レベル：3
* 構成：API仕様
* トーン：ビジネス
* 形式：json
* セクション：summary, prompt, reflection
* 連鎖：ON
* 属性：開発者
* 目的：Slack連携

生成CLI：

```
gpt-tutor --level 3 --structure API仕様 --tone business --format json --section summary+prompt+reflection --chain true --persona 開発者 --purpose Slack連携
```

---

## 💡 GUI連携のポイント

* CLI／DSL構文にリアルタイム変換可能な設計に
* 入力ガイド付きUI（例：hoverで説明）で初心者支援
* 上記フィールドに沿ってNotion/Figmaにフォームを構成

最終更新日：2025年5月13日
