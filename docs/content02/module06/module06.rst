レポート生成
================================================

セキュリティ レポートを作成、複製し、WAF ポリシーによって処理されたトラフィック、またはアプリケーションによって受信されたトラフィックに基づいてセキュリティ レポートの概要を生成します。

.. note::
   セキュリティ レポートは、生成された概要に対して構成されたデータおよびオブジェクト設定です。セキュリティ レポートを作成するときは、構成を作成することになります。選択したセキュリティ レポートに基づいてセキュリティ レポートの概要を生成します。

前提条件¶
-------------------------------------------------
アプリケーションまたはポリシーで検出されたトラフィックに基づいてレポートを生成するには、次のものが必要です。

- 1 つ以上の WAF ポリシーが設定されています。
- WAF ポリシーは、BIG-IP Next インスタンスにデプロイされたアプリケーションにアタッチされます。
- WAF で保護されたアプリケーションがトラフィックを受信して​​います。


CM画面左上部のworkspaceから、"Security" > "Reports" を選択します。

レポート名をクリックし、"Generate Report" をクリックしてレポートを生成します。


   .. image:: images/Picture1.png
      :scale: 20%
      :align: center
   |


レポートの設定を確認します。


   .. image:: images/Picture2.png
      :scale: 30%
      :align: center
   |


PDFで保存します。

   .. image:: images/Picture3.png
      :scale: 30%
      :align: center
   |

BIG-IP Next Central Manager は、一般的な監視対象の保護手段、トラフィック パターン、WAF 攻撃に対する悪意のある脅威インジケーターを含むセキュリティ レポート テンプレートを提供します。

次の表に、各テンプレートに含まれる情報の概要を示します。これらのテンプレートは変更または削除できませんが、テンプレートを複製してカスタム レポートを作成することはできます。クローン レポートを作成およびカスタマイズする方法については、 `Clone a security report`_  を参照してください。

各セキュリティ レポート テンプレートに含まれる詳細情報は次のとおりです。セキュリティ報告の概要を生成すると、上位の結果は、攻撃されたアプリケーション (全体) の上位に基づいて表示され、続いてカテゴリ選択ごとの上位のアプリケーションが表示されます。生成されたセキュリティ レポートの概要では、最後の期間と前の期間のレポートが比較されます。

各テンプレート レポートには、すべての保護されたアプリケーションからの情報が含まれます。


.. list-table:: Security Report テンプレート
   :widths: 25 50
   :header-rows: 1

   * - テンプレート名
     - 説明
   * - Full report across all categories
     - すべてのアプリケーションおよびカテゴリにわたる上位の攻撃アクティビティに関する完全なレポート
   * - Top attacked applications
     - 攻撃された上位のアプリケーションの結果を表示するレポート
   * - Top attacked URL
     - すべての保護されたアプリケーション全体で最も攻撃された URL
   * - Top malicious bots
     - すべてのアプリケーションで最も検出される悪意のあるボットのシグネチャ
   * - Top malicious IP (IPI)
     - すべてのアプリケーションで最も検出される悪意のある IP (IPI) アドレス
   * - Top protection types
     - すべてのアプリケーションで最もブロックされるViolationとシグネチャ
   * - Top source IPs attackers
     - すべてのアプリケーションで攻撃が検出されたリクエストを含む上位の送信元 IP と国
   * - Top threat campaigns
     - すべてのアプリケーションで最も頻繁に検出される攻撃キャンペーン



.. _Clone a security report: https://clouddocs.f5.com/bigip-next/20-1-0/waf_management/cm_awaf_how_to_security_reports.html#clone-a-security-report



