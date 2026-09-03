# A2Z Blueprint

> **A → Z, 26 viewpoints, one system.**

ソフトウェアを設計するとき、巨大な設計書を一冊作るのではなく、26枚の小さな設計書に分解する。

A2Z Blueprint は、A〜Zの26の視点から同じシステムを観察し、設計漏れ・矛盾・未決定事項を見つけるための設計フレームワークです。

## A–Z

| | Viewpoint | 問うこと |
|---|---|---|
| A | Architecture | どう分割するか |
| B | Business | 何の価値を生むか |
| C | Concept | 何を意味するか |
| D | Data | 何を持つか |
| E | Entity | 何が存在するか |
| F | Flow | 何がどう流れるか |
| G | Graph | 何と何がつながるか |
| H | Human | 誰が関わるか |
| I | Interface | どこで接するか |
| J | Job | 何を実行するか |
| K | KPI | 何を測るか |
| L | Logic | どう判断するか |
| M | Model | 何をモデル化するか |
| N | Network | どう接続するか |
| O | Operation | どう運用するか |
| P | Process | どういう手順か |
| Q | Quality | どの品質を保証するか |
| R | Requirement | 何を満たすべきか |
| S | Security | 何を守るか |
| T | Test | どう証明するか |
| U | UX | どう感じ、使うか |
| V | Version | どう変化するか |
| W | Workflow | どう仕事を流すか |
| X | External | 外部とどう関わるか |
| Y | YAML | 何を設定として宣言するか |
| Z | Zero | 何もない状態・初期状態は何か |

## 設計の中心線

26枚は独立したチェックリストではありません。中心となる設計連鎖があります。

```text
Requirement
    ↓
Concept
    ↓
Architecture
    ↓
Entity → Data → Flow → Interface
    ↓
Logic → Process → Workflow
    ↓
Test
```

Business / Human / UX / Security / Quality / Operation / External などが、この中心線を横断して制約・価値・利用者・運用条件を与えます。

## Ontology

[`ontology.json`](./ontology.json) が A2Z Blueprint の機械可読な定義です。

Ontology の目的は、26個のファイルを分類することではありません。

**「同じSystemを26の異なる視点から見る」ための関係モデル**を定義します。

## 1枚の設計書

各設計書はできるだけ小さく保ちます。

```markdown
# A — Architecture

## Purpose
## Decision
## Context
## Diagram
## Constraints
## Alternatives
## Consequences
## Open Issues
```

## Agentとの関係

A2Z Blueprint は人間だけの設計書ではありません。

Agent が A→Z を順番に読むことで、

```text
A–Z Blueprint
      ↓
設計上の不足・矛盾を発見
      ↓
Issue
      ↓
Implementation
      ↓
Test
```

という設計→実装のループを作れます。

## 原則

- **26枚に固定する** — 増やす前に既存の視点で表現できないか考える
- **1枚1観点** — 一つの文書に複数の責務を混ぜない
- **関係を重視する** — ファイル単体よりA–Z間の関係を見る
- **決定を残す** — 設計書は説明文ではなくDecision Logでもある
- **小さく保つ** — Agentが全体を一度に扱えるサイズを目指す

## Status

**Experimental / v0.1.0**

A2Z Blueprint は完成した方法論ではなく、実際のプロジェクトで使いながら育てる設計Ontologyです。
