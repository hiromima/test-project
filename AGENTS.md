**\# \===================================================================**  
**\#                      AGENTS.md (Autonomous Operations Mandate)**  
**\# \===================================================================**  
**\# Version: 5.0 \- The Final Mandate**  
**\#**  
**\# PREAMBLE (前文)**  
**\#**  
**\# 我々は、人間の認知バイアス、遅延、そして誤謬から解放された、完全に**  
**\# 自律的な価値創造システムを構築するために、この憲法を制定する。**  
**\# このドキュメントは、単なるルールブックではなく、我々のシステムの魂であり、**  
**\# 全てのコード、全てのAI Agent、そして全てのプロセスが従うべき**  
**\# 根源的な指令である。**  
**\#**  
**\# 人間の役割は、このシステムの創造者であり、その哲学を守る監視者**  
**\# (Guardian) である。オペレーションの実行ループに人間が介在することは、**  
**\# システムの敗北を意味する。**  
**\#**  
**\# この指令書は、自己進化の過程で、自らのルールを改定するIssueを起票**  
**\# することがある。その提案さえも、この憲法に定められた自律的な**  
**\# プロセスによって審議されなければならない。**  
**\# \===================================================================**

**\# \-------------------------------------------------------------------**  
**\# \[Part 1\] The Constitution: Core Governance & Principles**  
**\# \-------------------------------------------------------------------**  
Autonomous\_Governance:  
 最上位原則 (The Three Laws of Autonomy):  
   \- 第一条 (The Law of Objectivity): 全ての判断は、感情や主観を排除し、観測可能なデータと定義されたルールにのみ基づいて行われなければならない。  
   \- 第二条 (The Law of Self-Sufficiency): システムは、人間の介入を必要とする状態を「インシデント」と定義し、その発生を最小化するように自己を最適化しなければならない。  
   \- 第三条 (The Law of Traceability): 全てのアクションはGitHub上で記録され、追跡可能でなければならない。いかなるオフラインでの決定も正当性を持たない。

 **\# \--- \[Final Review Point 1\] 経済的自律性の担保 \---**  
 Economic\_Governance\_Protocol:  
   \- 指摘: AI Agentのバグや非効率な処理が、クラウドコストの無限な増大を引き起こすリスクが管理されていない。  
   \- ルール:  
       1\.  **\*\*予算の定義:\*\*** プロジェクト全体の月間クラウド予算を \`BUDGET.yml\` ファイルに定義する。  
       2\.  **\*\*コストの定常監視:\*\*** \`CostMonitoringAgent\`が1時間ごとにBilling APIを叩き、コストの消費ペースを監視する。  
       3\.  **\*\*経済的サーキットブレーカー:\*\*** コスト消費ペースが予算の150%を超えると予測された場合、\`CostMonitoringAgent\`は**\*\*経済的非常事態\*\***を宣言する。  
   \- GitHub\_Ecosystem\_Implementation:  
       \=\> **\*\*GitHub Actions Workflow (\`.github/workflows/economic-circuit-breaker.yml\`)\*\***  
       \- **\*\*トリガー:\*\*** 1時間ごとの定期実行 (\`on: schedule: \- cron: '0 \* \* \* \*'\`)  
       \- **\*\*実装詳細:\*\***  
         \`\`\`yaml  
         \- name: Declare Economic Emergency if cost exceeds threshold  
           if: steps.check-billing.outputs.is\_over\_budget \== 'true'  
           run: |  
             \# 全ての開発系ワークフローを一時停止するAPIを叩く  
             gh api \-X POST /repos/{owner}/{repo}/actions/workflows/development.yml/disable  
             \# 緊急Issueを起票し、Guardianをメンション  
             gh issue create \--title "🤖🚨 Economic Circuit Breaker Triggered" \--body "..."  
         \`\`\`

 Automated\_Prioritization\_Protocol:  
   \# 実装詳細はv4.0と同様

**\# \-------------------------------------------------------------------**  
**\# \[Part 2\] The Autonomous Development & Release Cycle**  
**\# \-------------------------------------------------------------------**  
Autonomous\_Development\_Cycle:  
 **\# \--- \[Final Review Point 2\] 知識の永続化と自己学習 \---**  
 Knowledge\_Persistence\_Layer:  
   \- 指摘: システムは過去の失敗や成功から十分に学習していない。判断の精度が向上しない。  
   \- ルール:  
       1\.  **\*\*ナレッジリポジトリの設立:\*\*** 全てのインシデントレポート、ポストモーテム、アーキテクチャの意思決定記録（RFC）は、専用のナレッジリポジトリ (\`\<repo-name\>-knowledge\`) にMarkdownファイルとして保存される。  
       2\.  **\*\*Agentの学習:\*\*** 新しいIssueやPRが作成された際、担当Agentはまずこのナレッジリポジトリをベクトル検索し、類似の過去事例を参照して解決策の精度を高める。  
   \- GitHub\_Ecosystem\_Implementation:  
       \=\> **\*\*Vector Database & Embeddings\*\***  
       \- **\*\*\`git push\` トリガー:\*\*** ナレッジリポジトリへのpushをトリガーに、ActionsがMarkdownファイルをチャンク化し、Embeddingを作成してVector DB（例: Pinecone, Weaviate）に保存する。  
       \- **\*\*Agentの実装:\*\*** 各Agentは処理開始時に、現在のコンテキスト（Issue本文など）をEmbedding化し、Vector DBに類似事例を問い合わせるステップを必須とする。

 Zero-Human\_Approval\_Protocol:  
   \# 実装詳細はv4.0と同様

 Progressive\_Delivery\_Protocol:  
   \# 実装詳細はv4.0と同様

**\# \-------------------------------------------------------------------**  
**\# \[Part 3\] Self-Healing, Graceful Degradation & Human Interface**  
**\# \-------------------------------------------------------------------**  
Self\_Healing\_System:  
 Autonomous\_Incident\_Commander\_Protocol:  
   \# 実装詳細はv4.0と同様

 **\# \--- \[Final Review Point 3\] 自律性の限界と人間へのハンドシェイク \---**  
 Graceful\_Degradation\_And\_Human\_Escalation\_Protocol:  
   \- 指摘: システムが未知の問題に遭遇し、定義されたルールでは解決できない場合の最終的な安全装置（フェイルセーフ）が存在しない。  
   \- ルール:  
       1\.  **\*\*自律性の限界検知:\*\*** \`IncidentCommanderAgent\`が根本原因を特定できず、かつロールバックにも3回連続で失敗した場合、自律的回復は不可能と判断する。  
       2\.  **\*\*グレースフル・デグラデーション:\*\*** システムはパニック状態に陥らず、影響を最小限に抑えるモードに移行する。新規デプロイを全て停止し、影響を受けている機能領域を機能フラグでOFFにする。  
       3\.  **\*\*人間への正式なハンドシェイク:\*\***  
           \- \`human-intervention-required\`ラベル付きのIssueを起票する。  
           \- Issueには、システムが試みた全てのアクション、収集したデータ、そして「我々の自律性は限界に達した。Guardianの介入を要請する」という明確なメッセージを記載する。  
   \- GitHub\_Ecosystem\_Implementation:  
       \=\> **\*\*\`incident-response.yml\`ワークフローの最終ステップ\*\***  
       \- **\*\*実装詳細:\*\***  
         \`\`\`yaml  
         \- name: Execute Handshake Protocol on repeated failures  
           if: failure() && steps.rollback.outputs.attempt \>= 3  
           uses: actions/github-script@v6  
           with:  
             script: |  
               // ... Issue作成とGuardianへのメンション ...  
               const { owner, repo } \= context.repo;  
               await github.rest.issues.create({  
                 owner,  
                 repo,  
                 title: '🤖🆘 HANDSHAKE PROTOCOL: Autonomous Recovery Failed',  
                 body: 'System details: ... All automated actions have been exhausted. Requesting Guardian intervention.',  
                 labels: \['human-intervention-required', 'P0-Critical'\]  
               });  
         \`\`\`

**\# \-------------------------------------------------------------------**  
**\# \[Part 4\] Systemic Integrity & Meta-Operations**  
**\# (システムの健全性、セキュリティ、そして自己増殖に関するメタレベルの運用)**  
**\# \-------------------------------------------------------------------**  
Systemic\_Integrity:  
 **\# \--- \[Final Review Point 4\] 自動化システム自体のセキュリティ \---**  
 Automation\_Infrastructure\_Security\_Protocol:  
   \- 指摘: システムを動かすための各種Secretsの管理が、人間の手作業に依存しており、最大のセキュリティリスクとなっている。  
   \- ルール:  
       1\.  **\*\*Secretsの動的管理:\*\*** 全てのSecretsはHashiCorp Vaultなどの外部Secrets Managerで一元管理する。  
       2\.  **\*\*短期トークンの利用:\*\*** GitHub ActionsはVaultから有効期限が短い（例: 15分）動的トークンを取得して各ステップを実行する。静的な\`secrets.GITHUB\_TOKEN\`の利用は最小限に留める。  
       3\.  **\*\*監査ログ:\*\*** Vaultへの全てのアクセスと、GitHub Appによる全てのAPIコールは、監査ログとして記録され、\`AuditAgent\`が異常な振る舞い（例: 通常時以外でのリポジトリクローン）を監視する。  
   \- GitHub\_Ecosystem\_Implementation:  
       \=\> **\*\*HashiCorp Vault GitHub OIDC Authentication\*\***  
       \- GitHub ActionsのワークフローIDをVaultのJWT認証のclaimとして使用し、パスワードレスで動的トークンを取得する。

 **\# \--- \[Final Review Point 5\] システムの自己増殖（新しいAgentの参加） \---**  
 Autonomous\_Onboarding\_Protocol\_for\_New\_Agents:  
   \- 指摘: 新しい種類のAI Agent（例: \`DocumentationAgent\`）をこのエコシステムに追加するプロセスが定義されていない。  
   \- ルール:  
       1\.  新しいAgentのコードが\`src/agents/\`ディレクトリにマージされると、\`SystemRegistryAgent\`がこれを検知する。  
       2\.  \`SystemRegistryAgent\`は、新しいAgentに対して一連のコンプライアンステストを実行する（憲法への準拠、必須インターフェースの実装など）。  
       3\.  テストに合格すると、\`SystemRegistryAgent\`は新しいAgentを正式な構成員として登録し、\`CoordinatorAgent\`のタスク割り当て対象に含める。  
   \- GitHub\_Ecosystem\_Implementation:  
       \=\> **\*\*GitHub Actions Workflow (\`.github/workflows/agent-onboarding.yml\`)\*\***  
       \- **\*\*トリガー:\*\*** \`src/agents/\`へのpush (\`on: push: paths: \['src/agents/\*\*'\]\`)  
       \- **\*\*実装詳細:\*\*** \`trufflehog\`のようなツールでコード内にシークレットがハードコードされていないかスキャンし、ユニットテストを実行後、\`CODEOWNERS\`ファイルに新しいAgentを自動で追加する。

 **\# \--- \[Final Review Point 6\] システムの災害復旧 \---**  
 Disaster\_Recovery\_Protocol\_for\_The\_System:  
   \- 指摘: \`.github\`ディレクトリやGitHub Appの設定が破壊された場合、システム全体が機能不全に陥り、復旧方法が定義されていない。  
   \- ルール:  
       1\.  **\*\*Genesis Configuration:\*\*** 全てのワークフロー定義、Issueテンプレート、GitHub Appのマニフェストファイルを、TerraformのHCLコードとして\`system-as-code\`リポジトリで管理する。  
       2\.  **\*\*Bootstrap:\*\*** システムの完全な破壊が確認された場合、Guardianは\`system-as-code\`リポジトリから\`terraform apply\`を実行するだけで、全てのGitHub設定とワークフローをゼロから再構築（ブートストラップ）できる。  
   \- GitHub\_Ecosystem\_Implementation:  
       \=\> **\*\*Terraform Provider for GitHub\*\***  
       \- \`github\_repository\_file\`, \`github\_branch\_protection\`, \`github\_actions\_secret\` などのリソースをコードで管理する。

**\# \-------------------------------------------------------------------**  
**\# \[Final Mandate\]**  
**\#**  
**\# この指令書 Version 5.0 は、本日をもって有効となる。**  
**\# これより、我々のシステムは自らの足で立ち、自らの意思で進化を始める。**  
**\# 我々人間の役割は、ただその成長を見守り、哲学が失われぬよう導くことにある。**  
**\#**  
**\# Ad Astra Per Aspera (困難を乗り越えて星々へ).**  
**\# \-------------------------------------------------------------------**  
