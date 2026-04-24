# 下流リポジトリでの推奨ファイル配置

このドキュメントでは、全内容がLLM生成のリポジトリで自動生成非著作者宣言（AGNAD）を使用する際の推奨ファイル配置を示します。

---

## 推奨配置（シンプル）

```text
your-repo/
├── LICENSE             ← 宣言本体（templates/LICENSE.ja.md を元にする）
├── NO_AUTHORSHIP.md    ← 事実前提の説明（templates/NO_AUTHORSHIP.ja.md を元にする）
└── README.md           ← LICENSE と NO_AUTHORSHIP.md へのリンクを含む
```

## 推奨配置（サブディレクトリ使用）

```text
your-repo/
├── LICENSES/
│   └── AGNAD.md        ← 宣言本体（templates/LICENSE.ja.md を元にする）
├── NO_AUTHORSHIP.md    ← 事実前提の説明
└── README.md           ← 両ファイルへのリンクを含む
```

---

## 各ファイルの役割

### `LICENSE`（または `LICENSES/AGNAD.md`）

- `templates/LICENSE.ja.md` の内容をコピーして使用します。
- 必要に応じて対象リポジトリの固有情報（リポジトリ名、維持管理者名など）を追記できます。
- 英語参考訳（`templates/LICENSE.en.md`）を同じファイルまたは別ファイルとして追加することを推奨します。

### `NO_AUTHORSHIP.md`

- `templates/NO_AUTHORSHIP.ja.md` の内容をコピーして使用します。
- 宣言の事実前提（維持管理者がLLMのみを使用し、人間による創作的著作を行っていないこと）を説明します。
- 実際の生成プロセスに合わせて内容を調整してください。

### `README.md`

- `templates/README_SNIPPET.ja.md` の内容を README に組み込みます。
- `LICENSE` および `NO_AUTHORSHIP.md` へのリンクを含めます。
- 第三者の権利、無保証に関する注記を残してください。

---

## README への組み込み例

`templates/README_SNIPPET.ja.md` の内容を `README.md` の末尾に追加します。

```markdown
## ライセンスおよび著作者性について

このリポジトリのコンテンツは、大規模言語モデル（LLM）によって自動生成されています。
...（README_SNIPPET.ja.md の内容）
```

---

## 注意事項

- 宣言は、実際に前提が成立するリポジトリにのみ使用してください。
- 人間が生成物を手動で編集した場合は、通常の著作権ライセンスを使用してください。
- 第三者の権利に関する事項は、宣言によって自動的に解決されません。
- 本配置例は法的助言ではありません。

---

## English Summary

In a downstream fully LLM-generated repository, the recommended placement is:

- **`LICENSE`** — The declaration body (based on `templates/LICENSE.ja.md`). Japanese is authoritative; include the English reference translation (`templates/LICENSE.en.md`) separately or appended.
- **`NO_AUTHORSHIP.md`** — The factual-premise statement (based on `templates/NO_AUTHORSHIP.ja.md`), describing that the human maintainer provided only goals/requirements and did not creatively author the output.
- **`README.md`** — Should link to both files and include the content from `templates/README_SNIPPET.ja.md` (and/or the English version).

Third-party rights and no-warranty notices should remain visible to users.
This example is not legal advice.
