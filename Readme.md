# プロンプトエンジニアリングのベストプラクティス
forked from bskim/PromptEngineering
## 始める前に
1. VSCode 導入 https://code.visualstudio.com/Download
1. Python 導入 https://www.python.org/downloads/
1. Jupyter Notebook extension 導入 https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter
1. Python extension 導入 https://marketplace.visualstudio.com/items?itemName=ms-python.python
1. Github repo clone : 
1. Open Notebook
1. Download API Key and URL from the link : (will be expired :)
1. ラボ環境はインターネットに対応している必要があります。

## 諸注意
1. このラボでは、Prompt のベスト プラクティスとして他の Prompt ライブラリ/エンジン/フレームワーク/テンプレートの使用を最小限に抑え、Prompt 自体と Langchain を使用します。実際の実装では、Prompt Library/Engine/Framwork/Template を使用して、大規模な言語モデルに基づくアプリケーションの実装をはるかに簡単に行うことができます。
1. 便利な大規模言語モデル フレームワーク、プロンプト関連のフレームワーク、およびプロンプト エンジニアリングのベスト プラクティスについては、[このページ](./References.md) を参照してください。
1. このラボでは、LangChain、Python、Jupyter を使用しますが、これは LangChain セッションではありません。LangChainの基本機能のみを使って練習します。Stream 機能を使用すると、大規模な言語モデルの応答性を向上させ、よりリアルタイムの会話が可能になりますが、ラボでは Invoke を使用して応答を確認するだけです。これにより、リクエスト後にすべてのレスポンスが生成された後に結果を確認できますが、レスポンスの長さによっては、レスポンスが表示されるまでに数秒から数十秒かかる場合があります。
1. プロンプトエンジニアリングは、正確なエンジニアリングではなく、大規模な言語モデルが効果的に命令を実行できるように明確な指示をどのように記述するかに関するものであり、多くの試みと実験がまだ行われています。本日の演習では、代表的な事例をいくつかご紹介しますが、すべてを網羅することはできません。[このページ]その他のベスト プラクティスについては、(./References.md) を参照してください。 
1. ラボ環境の設定を容易にするため、別途AzureサブスクリプションやAzure OpenAIの作成なしで練習できるように、デモにはAzure OpenAI GPT-4-oモデルを使用していますが、大規模なラボや実際のサービスを想定していないため、十分なスループットを保証するものではありません。トレーニングの参加者数によっては、スロットリングを体験できます。フィールド実習の参加者数に応じてグループを編成することで、リクエストの数を調整することができます。
1. ラボで使用した API キーと URL を引き続き使用することはできなくなります。トレーニング後に破壊されます。 
