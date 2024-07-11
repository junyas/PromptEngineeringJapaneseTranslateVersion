# 프롬프트 엔지니어링 모범사례 실습
## 준비사항
1. VSCode 설치 https://code.visualstudio.com/Download
1. Python 설치 https://www.python.org/downloads/
1. Jupyter Notebook extension 설치 https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter
1. Python extension 설치 https://marketplace.visualstudio.com/items?itemName=ms-python.python
1. Github repo clone : 
1. Open Notebook
1. Download API Key and URL from the link : (will be expired :)
1. 실습환경은 인터넷이 가능한 환경이어야 합니다.

## 실습전 알립니다.
1. 본 실습은 Prompt 모범사례를 위하여 다른 Prompt Library/Engine/Framework/Template의 사용을 최소화하고 Prompt 자체와 Langchain을 사용하여 진행합니다. 실제 구현시에는 Promprt Library/Engine/Framwork/Template을 사용하여 훨씬 용이하게 대형언어모델 기반의 애플리케이션을 구현할 수 있습니다. 
1. 몇가지 유용한 대형언어모델 Framework와 Prompt 관련 Framework들, Promprt Engineering 모범사례들은 [이 페이지](./References.md)를 참고하세요.
1. 본 실습에서는 LangChain과 Python, Jupyter를 사용하지만, LangChain 세션이 아닙니다. LangChain의 기본기능만을 사용하여 실습을 진행합니다. 대형언어모델의 응답성을 향상하고 보다 실시간적인 대화가 가능하도록 Stream기능을 사용할 수 있지만, 실습에서는 단순히 Invoke를 사용하여 응답을 확인합니다. 이로 인해 요청 후 응답이 모두 생성된 다음 결과를 확인할 수 있어 응답의 길이에 따라 응답을 확인하는데 수초에서 수십초가 걸릴 수 있습니다.
1. Prompt Engineering은 정밀한 Engineering이라기보다 얼마나 대형언어모델이 효과적으로 지시를 수행할 수 있도록 명확하게 지시를 작성할 수 있는가에 대한 요령에 가깝고, 수많은 시도와 실험들이 지금도 수행되고 있습니다. 오늘 실습에서는 그중 대표적인 몇가지 사례들을 소개합니다만 전체적인 부분을 모두 다룰 수는 없습니다. [이 페이지](./References.md)에서 추가적인 모범사례들을 확인하시기 바랍니다. 
1. 실습 환경의 구성 편의성을 위하여 별도의 Azure 구독이나 Azure OpenAI 생성없이 실습하실 수 있도록 Demo용 Azure OpenAI GPT-4-o model을 사용합니다만, 대규모 실습 용도나 실서비스용도가 아니라서, 충분한 throughput을 보장하지 않습니다. 실습 참여 인원에 따라서 Throttling을 경험하실 수 있습니다. 현장의 실습 참여인원에 따라 조를 구성하여 요청수를 조절할 수 있습니다.
1. 실습에 사용한 API key 및 URL은 개인적으로 계속 사용하실 수 없습니다. 실습 이후 파기될 예정입니다. 
