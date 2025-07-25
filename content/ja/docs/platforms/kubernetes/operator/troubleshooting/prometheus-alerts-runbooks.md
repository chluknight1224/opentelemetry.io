---
title: Prometheusアラートのランブック
default_lang_commit: fe623719bc24346e9dcd77e9769026cf1c720cc5
---

## マネージャールール {#manager-rules}

### ReconcileErrors {#reconcile-errors}

|      |                                                                                                                                          |
| ---: | ---------------------------------------------------------------------------------------------------------------------------------------- |
| 意味 | OpenTelemetryコレクターの構成が誤っている可能性があり、OpenTelemetryオペレーターがリコンシレーションステップを成功することができません。 |
| 影響 | すでに実行中または新しい正しいDeploymentには影響しません。                                                                               |
| 診断 | 発生する理由をマネージャーログで確認する。                                                                                               |
| 緩和 | エラーの原因となっているOpenTelemetryコレクターを特定し、構成を修正する。                                                                |

### WorkqueueDepth {#workqueue-depth}

|      |                                                                                                |
| ---: | ---------------------------------------------------------------------------------------------- |
| 意味 | オペレーターのワークキューが0より大きい。                                                      |
| 影響 | キューの深さがすぐに0に戻れば、影響はありません。問題が継続する場合は、さらに調査が必要です。  |
| 診断 | 発生する理由をマネージャーログで確認する。                                                     |
| 緩和 | 多くのエラーによって引き起こされている可能性があります。ログの内容に基づいてアクションします。 |
