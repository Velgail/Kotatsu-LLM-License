# 自動生成非著作者宣言（AGNAD）テンプレートリポジトリ

> **Automated Generation Non-Authorship Declaration (AGNAD) — Template Repository**

---

## このリポジトリについて

このリポジトリは、LLM（大規模言語モデル）またはその他の自動処理によって生成されたリポジトリ・コンテンツを対象とする、**非著作者宣言（自動生成非著作者宣言 / AGNAD）** の雛形文書セットを提供します。

このリポジトリ自体は **CC0 1.0 Universal** のもとで公開されています。
テンプレート文書を自由に複製・改変・翻訳・改称・再配布して利用できます。

---

## テンプレートの目的

以下の状況に該当するリポジトリ・コンテンツに対して使用できます。

- ソースコード、設定ファイル、ワークフロー、テンプレート、プロンプト、記事、要約、見出し、分類、説明文などがLLMにより生成されている。
- 人間の維持管理者は目的・要件・指示のみを提供した。
- 生成物の具体的な表現について、人間は創作的な執筆・選択・配置・編集・監督を行っていない。
- 維持管理者は生成物に対して著作者としての権利を主張しない。

---

## テンプレートが適合しない場合

以下のいずれかに該当する場合は、このテンプレートの前提が成立しない可能性があります。

- 人間が出力を手動で編集・修正・選択・整理・改善した。
- 人間がレイアウト、構成、表現を創作的に監督・制御した。
- 人間が著作物として認められる程度の創意工夫を加えた。

前提が成立しない場合は、通常の著作権ライセンスを検討してください。

---

## 第三者の権利について

このテンプレートは、第三者の権利（著作権、商標権、肖像権、パブリシティ権など）に影響を与えません。
LLM生成コンテンツが既存の著作物、商標、人物の肖像等を含む可能性がある場合は、別途検討が必要です。
引用・リンクされた外部素材の権利は、それぞれの権利者に帰属します。

---

## 法的助言ではない

このテンプレートおよびREADMEは情報提供を目的としており、法的助言ではありません。
具体的な法的問題については専門家にご相談ください。

---

## テンプレートの構成

```
templates/
  LICENSE.ja.md          ← 日本語正文（宣言本体）
  LICENSE.en.md          ← 英語参考訳
  NO_AUTHORSHIP.ja.md    ← 非著作者である事実前提の説明（日本語）
  NO_AUTHORSHIP.en.md    ← 英語参考訳
  README_SNIPPET.ja.md   ← 下流リポジトリのREADME用スニペット（日本語）
  README_SNIPPET.en.md   ← 英語参考訳
```

---

## 下流リポジトリでの配置例

下流リポジトリ（全内容がLLM生成のリポジトリ）では、以下のように配置することを推奨します。

**シンプルな配置例：**

```text
LICENSE
NO_AUTHORSHIP.md
README.md
```

**サブディレクトリを使う配置例：**

```text
LICENSES/
  AGNAD.md
NO_AUTHORSHIP.md
README.md
```

各ファイルの役割：

- `LICENSE` または `LICENSES/AGNAD.md` — 宣言本体（`templates/LICENSE.ja.md` を元にする）
- `NO_AUTHORSHIP.md` — 非著作者である事実前提の説明（`templates/NO_AUTHORSHIP.ja.md` を元にする）
- `README.md` — 両ファイルへのリンクを含む

詳細は [`examples/downstream-layout.md`](examples/downstream-layout.md) を参照してください。

---

## このリポジトリのライセンス

このリポジトリ（テンプレート文書を含む）は **CC0 1.0 Universal** のもとで提供されます。
詳細は [`LICENSE`](LICENSE) を参照してください。

---

## 改変版について

テンプレートを改変して使用する場合：

- 改変版を公式の原文として誤認させないようにしてください。
- 意図的に互換性を維持する場合を除き、名称変更・修正内容の明示を推奨します。

---

## English Summary

This repository provides a clean-room template document set — the **Automated Generation Non-Authorship Declaration (AGNAD)** — for repositories and contents generated entirely by LLMs or automated processing, where no human creative authorship exists in the concrete expression of the output.

**Key points:**

- The authoritative language of the template documents is **Japanese**.
- English versions are provided as reference translations only.
- This repository itself is released under **CC0 1.0 Universal**.
- The documents are templates; copy them into a downstream fully LLM-generated repository.
- **This is not legal advice.**
- The template applies only when the factual premise holds: the human maintainer provided only a goal or requirements, and did not creatively write, select, arrange, edit, or supervise the concrete expression of the generated files.
- Third-party rights (copyright, trademark, likeness, etc.) are outside the scope of this declaration and require separate consideration.
- See [`examples/downstream-layout.md`](examples/downstream-layout.md) for placement guidance.
