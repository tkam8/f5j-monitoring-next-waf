Violation Ratingの概要とVR=5の確認と対処方法
================================================

Violation Ratingに関する用語と概念をご説明します。

- Violation は WAF アルゴリズムによって評価され、攻撃と潜在的な誤検知アラートを区別しやすくなります。 
- Violation Rating は、セキュリティ アルゴリズムがViolationの存在に基づいてリクエストに割り当てる数値評価です。
- WAF ポリシー テンプレートに従って、 Violation Ratingが1、2、および 3 であっても要求はブロックされず、アラートのログのみが生成されます。
- Violation Ratingが4 または 5 の場合、リクエストはブロックされます。ブロック ページが表示され、ブロックされたステータスのトランザクションのログが生成されます。

詳細は以下のリンクをご参照ください。
https://clouddocs.f5.com/bigip-next/latest/waf_management/awaf_policy_violations.html 


次の表は、 Violation Ratingを解釈する方法を説明しています。

.. list-table:: Violation Rating
   :widths: 25 50
   :header-rows: 1

   * - Rating
     - 説明
   * - **5**
     - リクエストはおそらく脅威です。それに関連する学習エンジンによる提案をすべてクリアすることを検討してください。
   * - **4**
     - リクエストは脅威である可能性がありますが、提案を解消する前にさらなる調査が必要です。
   * - **3**
     - リクエストにはさらなる調査が必要です。
   * - **2**
     - リクエストは誤検知のように見えますが、さらなる調査が必要です。
   * - **1**
     - リクエストは誤検知である可能性が高いです。Learning Suggestionを受け入れて、これをセキュリティポリシーに追加することを検討してください。



CM画面左上部のworkspaceから、"Security" > "Monitoring" を選択します。

WAF Dashboardページの上部にある "Add Filter" をクリック


   .. image:: images/Picture1.png
      :scale: 20%
      :align: center
   |


"Violation Rating" > "is" > "5" を選択します。


   .. image:: images/Picture2.png
      :scale: 30%
      :align: center
   |


"Violations / Sub-Violations" 枠内にクリティカルのイベント表示を確認します。

   .. image:: images/Picture3.png
      :scale: 30%
      :align: center
   |


"View Logs" をクリックして、該当ログを確認します。

   .. image:: images/Picture4.png
      :scale: 30%
      :align: center
   |


"Violations / Sub-Violations" 枠内のクリティカルのイベントをクリックし、"Actions" をクリックします。

   .. image:: images/Picture5.png
      :scale: 30%
      :align: center
   |


"Enforcement Settings" の蘭からアクションを選択します。 (Alarm/ Alarm & Block/ Disable)

   .. image:: images/Picture6.png
      :scale: 30%
      :align: center
   |

"Apply To Policies" の一覧からポリシーを選択します。"Save & Deploy"を押して適用します。

   .. image:: images/Picture7.png
      :scale: 30%
      :align: center
   |

