# Project Plan: ハイエンド電動自転車ブランドコンセプト策定プロジェクト

## 🎯 Purpose
新発売されるハイエンド電動自転車（コアターゲット：クリエイター）のブランド理念を仮作成し、ブランドの意味構造化、表現モチーフ、コピーライティング、マーケティングプラン、および各種デザインアイテムの展開プランと方向性を策定する。

---

## Scope

### In Scope
- ブランド理念の仮作成
- ブランド意味の構造化（上位概念・下位概念）
- 表現モチーフの生成
- コピーライティングの生成
- マーケティングプランの生成
- 各種デザインアイテムの展開プランと方向性の策定

### Out of Scope
- 実際の製品開発
- 最終的なブランドロゴやデザインの制作
- 市場調査の実施
- 広告キャンペーンの実行

---

## 📈 Key Performance Indicators
- ブランド理念の明確性
- コンセプトの一貫性
- 提案されたデザイン方向性の多様性と実現可能性
- マーケティングプランの具体性と戦略性
- 意思決定者からの承認率

---

## 🤖 Agents

### **意思決定者** (人間)
**Description:** プロジェクトの最終的な方向性を決定し、主要な成果物を承認する責任を持つ。
**Responsibilities:**
- プロジェクト計画の承認
- 各フェーズの成果物のレビューと承認
- 最終的なブランドコンセプトとプランの承認

### **プロジェクト管理エージェント** (AI)
**Description:** プロジェクト全体の進行を管理し、タスクの割り当て、進捗の追跡、成果物の統合、レビュー準備を行う。
**Responsibilities:**
- 初期要件の分析とタスクバックログの作成
- 各エージェントへのタスク割り当てと進捗管理
- 生成された成果物の統合とレビュー準備
- プロジェクトの完了条件の監視

### **ブランド戦略エージェント** (AI)
**Description:** ブランドの核となる理念、価値、上位・下位概念を定義し、戦略的な方向性を策定する。
**Responsibilities:**
- ブランド理念の仮作成
- ブランド意味の上位・下位概念構造の定義
- ブランドのポジショニング戦略の提案

### **クリエイティブコンセプトエージェント** (AI)
**Description:** ブランドの視覚的・体験的な表現モチーフやムードボードを生成し、クリエイティブな方向性を示す。
**Responsibilities:**
- ブランドの表現モチーフ（色、形、質感、イメージなど）の生成
- ムードボードやビジュアルコンセプトの作成
- クリエイティブな方向性の提案

### **コピーライティングエージェント** (AI)
**Description:** ブランドのメッセージングを担い、ブランドスローガン、タグライン、主要なマーケティングコピーを生成する。
**Responsibilities:**
- ブランドスローガンとタグラインの作成
- ブランドのトーン＆マナーに沿ったコピーライティングの生成
- 主要なマーケティングメッセージの提案

### **マーケティングプランニングエージェント** (AI)
**Description:** ブランドのターゲットオーディエンス、ポジショニング、コミュニケーションチャネル、ローンチ戦略を含むマーケティングプランを策定する。
**Responsibilities:**
- ターゲットオーディエンスの定義と分析
- ブランドの市場ポジショニング戦略の策定
- コミュニケーションチャネルとプロモーション戦略の提案
- ローンチプランの概要作成

### **デザイン展開エージェント** (AI)
**Description:** ブランドコンセプトを具体的なデザインアイテムに落とし込むための展開プランと方向性を策定する。
**Responsibilities:**
- 製品デザイン言語の方向性策定
- パッケージデザインの方向性策定
- ウェブサイト、広告ビジュアルなどのデジタル・アナログデザインアイテムの展開プラン作成
- デザインガイドラインの骨子作成

---

## ⚙️ Workflow

### **Phase 0: 計画フェーズ**
- **Trigger:** 意思決定者が初期要件を提示する
- **Completion Condition:** 全ての初期タスクが起票され、意思決定者に承認されること
- **Iterative:** No

#### Stage: 計画立案
1. **Agent:** プロジェクト管理エージェント
   - **Instruction:** ユーザーの初期要件を分析し、このプロジェクトに必要なタスクを洗い出し、優先順位付けされたバックログを生成してください。
   - **Action:** 詳細なタスクバックログを作成
   - **Artifacts:**
     - **Type:** document
     - **Description:** プロジェクトバックログ
     - **Details:** `git_branch: feature/initial-backlog, git_commit: feat(project): Initial project backlog created, pull_request: Propose Initial Project Backlog`

### **Phase 1: ブランドコンセプト策定フェーズ**
- **Trigger:** 計画フェーズが完了し、バックログが承認される
- **Completion Condition:** 主要なブランドコンセプト要素（理念、意味構造、モチーフ、コピー）が意思決定者に承認されること
- **Iterative:** Yes

#### Stage: 概念生成と構造化
1. **Agent:** ブランド戦略エージェント
   - **Instruction:** クリエイターをコアターゲットとするハイエンド電動自転車のブランド理念を仮作成し、そのブランドの意味を上位概念と下位概念で構造化してください。
   - **Artifacts:**
     - **Type:** concept_draft
     - **Description:** ブランド理念と意味構造ドラフト
     - **Details:** `git_branch: concept/brand-philosophy, git_commit: feat(brand): Draft brand philosophy and meaning structure`

2. **Agent:** クリエイティブコンセプトエージェント
   - **Instruction:** ブランド理念と意味構造に基づき、クリエイター向けハイエンド電動自転車のブランドに相応しい表現モチーフ（色、形、質感、イメージなど）とビジュアルコンセプトを生成してください。
   - **Artifacts:**
     - **Type:** concept_draft
     - **Description:** 表現モチーフとビジュアルコンセプトドラフト
     - **Details:** `git_branch: concept/visual-motifs, git_commit: feat(creative): Draft expression motifs and visual concept`

3. **Agent:** コピーライティングエージェント
   - **Instruction:** ブランド理念と意味構造、および表現モチーフに基づき、ブランドスローガン、タグライン、および主要なマーケティングコピーのドラフトを生成してください。
   - **Artifacts:**
     - **Type:** concept_draft
     - **Description:** コピーライティングドラフト
     - **Details:** `git_branch: concept/copywriting, git_commit: feat(copy): Draft brand slogans and marketing copy`

#### Stage: 統合とレビュー
1. **Agent:** プロジェクト管理エージェント
   - **Instruction:** 生成されたブランド理念、意味構造、表現モチーフ、コピーライティングの各ドラフトを統合し、意思決定者によるレビューのための統合ドキュメントを作成してください。
   - **Artifacts:**
     - **Type:** document
     - **Description:** 統合ブランドコンセプトレビュー資料
     - **Details:** `git_branch: review/integrated-concept, git_commit: feat(review): Prepare integrated brand concept for review`

2. **Agent:** 意思決定者
   - **Instruction:** 統合ブランドコンセプトレビュー資料を確認し、承認または具体的なフィードバックを提供してください。
   - **Artifacts:**
     - **Type:** document
     - **Description:** ブランドコンセプト承認/フィードバック
     - **Details:** `git_branch: approval/concept-feedback, git_commit: docs(approval): Brand concept reviewed and feedback provided`

### **Phase 2: 展開プランニングフェーズ**
- **Trigger:** ブランドコンセプト策定フェーズが完了し、主要コンセプトが承認される
- **Completion Condition:** 全てのプラン（マーケティング、デザイン展開）が意思決定者に承認され、プロジェクトが完了すること
- **Iterative:** Yes

#### Stage: プランニングと方向性策定
1. **Agent:** マーケティングプランニングエージェント
   - **Instruction:** 承認されたブランド理念、意味構造、表現モチーフ、コピーライティングに基づき、マーケティングプラン（ターゲット、ポジショニング、チャネル、ローンチ戦略など）を策定してください。
   - **Artifacts:**
     - **Type:** plan_draft
     - **Description:** マーケティングプランドラフト
     - **Details:** `git_branch: plan/marketing-plan, git_commit: feat(marketing): Draft marketing plan`

2. **Agent:** デザイン展開エージェント
   - **Instruction:** 承認されたブランドコンセプトに基づき、製品デザイン言語、パッケージデザイン、ウェブサイト、広告ビジュアルなど、各種デザインアイテムの展開プランと具体的な方向性を策定してください。
   - **Artifacts:**
     - **Type:** plan_draft
     - **Description:** デザイン展開プランと方向性ドラフト
     - **Details:** `git_branch: plan/design-deployment, git_commit: feat(design): Draft design deployment plan and direction`

#### Stage: 最終レビューと承認
1. **Agent:** プロジェクト管理エージェント
   - **Instruction:** マーケティングプランとデザイン展開プランを統合し、意思決定者による最終レビューのための統合ドキュメントを作成してください。
   - **Artifacts:**
     - **Type:** document
     - **Description:** 統合プラン最終レビュー資料
     - **Details:** `git_branch: review/final-plans, git_commit: feat(review): Prepare integrated final plans for review`

2. **Agent:** 意思決定者
   - **Instruction:** 統合最終プランレビュー資料を確認し、マーケティングプランとデザイン展開プランについて最終的な承認または具体的なフィードバックを提供してください。
   - **Artifacts:**
     - **Type:** document
     - **Description:** 最終プラン承認/フィードバック
     - **Details:** `git_branch: approval/final-plan-feedback, git_commit: docs(approval): Final plans reviewed and feedback provided`
