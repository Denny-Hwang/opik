<div align="center"><b><a href="README.md">English</a> | <a href="readme_CN.md">简体中文</a> | <a href="readme_ES.md">Español</a> | <a href="readme_FR.md">Français</a> | <a href="readme_DE.md">Deutsch</a> | <a href="readme_JA.md">日本語</a> | <a href="readme_KO.md">한국어</a></b></div>

> 참고: 이 파일은 AI로 기계 번역되었습니다. 더 나은 번역을 위한 개선을 환영합니다!


<h1 align="center" style="border-bottom: none">
    <div>
        <a href="https://www.comet.com/site/products/opik/?from=llm&utm_source=opik&utm_medium=github&utm_content=header_img&utm_campaign=opik"><picture>
            <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/comet-ml/opik/refs/heads/main/apps/opik-documentation/documentation/static/img/logo-dark-mode.svg">
            <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/comet-ml/opik/refs/heads/main/apps/opik-documentation/documentation/static/img/opik-logo.svg">
            <img alt="Comet Opik logo" src="https://raw.githubusercontent.com/comet-ml/opik/refs/heads/main/apps/opik-documentation/documentation/static/img/opik-logo.svg" width="200" />
        </picture></a>
        <br>
        Opik: 오픈 소스 LLM 관측성, 평가 및 AI 에이전트 추적
    </div>
</h1>
<p align="center">
<b>Opik은 AI 에이전트 추적, LLM 평가, 프롬프트 관리 및 프로덕션 모니터링을 위한 오픈 소스 LLM 관측성·평가 플랫폼입니다.</b> <a href="https://www.comet.com?from=llm&utm_source=opik&utm_medium=github&utm_content=what_is_opik_link&utm_campaign=opik">Comet</a>이 개발했습니다. Apache-2.0 라이선스로 전체 플랫폼을 무료로 자체 호스팅할 수 있으며 GitHub 스타가 20,000개 이상입니다.
</p>

<div align="center">

[![Python SDK](https://img.shields.io/pypi/v/opik)](https://pypi.org/project/opik/)
[![License](https://img.shields.io/github/license/comet-ml/opik)](https://github.com/comet-ml/opik/blob/main/LICENSE)
[![Build](https://github.com/comet-ml/opik/actions/workflows/build_apps.yml/badge.svg)](https://github.com/comet-ml/opik/actions/workflows/build_apps.yml)
<!-- [![Quick Start](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/comet-ml/opik/blob/main/apps/opik-documentation/documentation/docs/cookbook/opik_quickstart.ipynb) -->

</div>

<p align="center">
    <a href="https://www.comet.com/site/products/opik/?from=llm&utm_source=opik&utm_medium=github&utm_content=website_button&utm_campaign=opik"><b>웹사이트</b></a> •
    <a href="https://chat.comet.com"><b>Slack 커뮤니티</b></a> •
    <a href="https://x.com/Cometml"><b>Twitter</b></a> •
    <a href="https://www.comet.com/docs/opik/changelog"><b>변경 로그</b></a> •
    <a href="https://www.comet.com/docs/opik/?from=llm&utm_source=opik&utm_medium=github&utm_content=docs_button&utm_campaign=opik"><b>문서</b></a>
</p>

<p align="center"><sub>마지막 업데이트: 2026-07-17</sub></p>

<div align="center" style="margin-top: 1em; margin-bottom: 1em;">
<a href="#-what-is-opik">🚀 Opik이란?</a> • <a href="#-quick-start">⚡ 빠른 시작</a> • <a href="#-how-opik-compares">📊 Opik 비교</a> • <a href="#-frequently-asked-questions">❓ 자주 묻는 질문</a> • <a href="#%EF%B8%8F-opik-server-installation">🛠️ Opik 서버 설치</a> • <a href="#-opik-client-sdk">💻 Opik 클라이언트 SDK</a> • <a href="#-logging-traces-with-integrations">📝 트레이스 기록</a><br>
<a href="#-llm-as-a-judge-metrics">🧑‍⚖️ LLM 심사</a> • <a href="#-evaluating-your-llm-application">🔍 애플리케이션 평가</a> • <a href="#-star-us-on-github">⭐ 스타 남기기</a> • <a href="#-contributing">🤝 기여하기</a>
</div>

<br>

[![Opik 플랫폼 스크린샷(썸네일)](readme-thumbnail-new.png)](https://www.comet.com/signup?from=llm&utm_source=opik&utm_medium=github&utm_content=readme_banner&utm_campaign=opik)

<a id="-what-is-opik"></a>
## 🚀 Opik이란?

Opik은 LLM 앱과 AI 에이전트를 구축하는 팀을 위해 개발 단계의 첫 트레이스부터 프로덕션 모니터링까지 LLM 애플리케이션의 전체 수명 주기를 지원합니다. 주요 기능은 다음과 같습니다.

- **AI 에이전트 추적 및 관측성**: 다단계 에이전트와 도구 호출의 전체 트레이스 트리를 포함해 LLM 호출, 대화 및 에이전트 활동을 상세히 추적합니다.
- **LLM 평가**: 데이터셋, 실험 및 LLM 심사 지표를 통해 환각 탐지, 콘텐츠 검토 및 RAG를 평가합니다.
- **프롬프트 및 에이전트 최적화**: Opik Agent Optimizer SDK로 프롬프트와 에이전트를 개선합니다.
- **프로덕션용 모니터링**: 확장 가능한 대시보드와 온라인 평가 규칙을 제공합니다.
- **Opik Guardrails**: 안전하고 책임감 있는 AI 관행을 구현하도록 돕습니다.
- **CI/CD 평가**: PyTest 통합으로 커밋할 때마다 LLM 파이프라인을 테스트합니다.

<br>

주요 역량은 다음과 같습니다.

- **개발 및 추적:**
  - 개발 및 프로덕션 환경에서 모든 LLM 호출과 트레이스를 상세한 컨텍스트와 함께 추적합니다([빠른 시작](https://www.comet.com/docs/opik/quickstart/?from=llm&utm_source=opik&utm_medium=github&utm_content=quickstart_link&utm_campaign=opik)).
  - 폭넓은 서드 파티 통합으로 손쉽게 관측성을 확보합니다. 계속 늘어나는 프레임워크 목록과 원활하게 통합되며 **Google ADK**, **Autogen**, **Flowise AI** 등 널리 쓰이는 주요 프레임워크를 기본 지원합니다. ([통합](https://www.comet.com/docs/opik/integrations/overview/?from=llm&utm_source=opik&utm_medium=github&utm_content=integrations_link&utm_campaign=opik))
  - [Python SDK](https://www.comet.com/docs/opik/tracing/advanced/annotate_traces/#annotating-traces-and-spans-using-the-sdk?from=llm&utm_source=opik&utm_medium=github&utm_content=sdk_link&utm_campaign=opik) 또는 [UI](https://www.comet.com/docs/opik/tracing/advanced/annotate_traces/#annotating-traces-through-the-ui?from=llm&utm_source=opik&utm_medium=github&utm_content=ui_link&utm_campaign=opik)에서 트레이스와 스팬에 피드백 점수를 추가합니다.
  - [프롬프트 플레이그라운드](https://www.comet.com/docs/opik/development/prompt-playground)에서 프롬프트와 모델을 실험합니다.

- **평가 및 테스트**:
  - [데이터셋](https://www.comet.com/docs/opik/evaluation/advanced/manage_datasets/?from=llm&utm_source=opik&utm_medium=github&utm_content=datasets_link&utm_campaign=opik)과 [실험](https://www.comet.com/docs/opik/evaluation/advanced/evaluate_your_llm/?from=llm&utm_source=opik&utm_medium=github&utm_content=eval_link&utm_campaign=opik)으로 LLM 애플리케이션 평가를 자동화합니다.
  - 강력한 LLM 심사 지표를 활용해 [환각 탐지](https://www.comet.com/docs/opik/evaluation/metrics/hallucination/?from=llm&utm_source=opik&utm_medium=github&utm_content=hallucination_link&utm_campaign=opik), [콘텐츠 검토](https://www.comet.com/docs/opik/evaluation/metrics/moderation/?from=llm&utm_source=opik&utm_medium=github&utm_content=moderation_link&utm_campaign=opik), RAG 평가([답변 관련성](https://www.comet.com/docs/opik/evaluation/metrics/answer_relevance/?from=llm&utm_source=opik&utm_medium=github&utm_content=alex_link&utm_campaign=opik), [컨텍스트 정밀도](https://www.comet.com/docs/opik/evaluation/metrics/context_precision/?from=llm&utm_source=opik&utm_medium=github&utm_content=context_link&utm_campaign=opik)) 같은 복잡한 작업을 수행합니다.
  - [PyTest 통합](https://www.comet.com/docs/opik/evaluation/overview/?from=llm&utm_source=opik&utm_medium=github&utm_content=pytest_link&utm_campaign=opik)으로 평가를 CI/CD 파이프라인에 통합합니다.

- **프로덕션 모니터링 및 최적화**:
  - 대량의 프로덕션 트레이스를 기록합니다. Opik은 하루 4천만 개 이상의 트레이스를 처리하도록 설계되었습니다.
  - [Opik 대시보드](https://www.comet.com/docs/opik/tracing/dashboards/production_monitoring/?from=llm&utm_source=opik&utm_medium=github&utm_content=dashboard_link&utm_campaign=opik)에서 시간에 따른 피드백 점수, 트레이스 수 및 토큰 사용량을 모니터링합니다.
  - LLM 심사 지표가 포함된 [온라인 평가 규칙](https://www.comet.com/docs/opik/production/online-evaluation/rules/?from=llm&utm_source=opik&utm_medium=github&utm_content=dashboard_link&utm_campaign=opik)으로 프로덕션 문제를 식별합니다.
  - **Opik Agent Optimizer**와 **Opik Guardrails**를 활용해 프로덕션 LLM 애플리케이션을 지속적으로 개선하고 보호합니다.

**대상 사용자:** LLM 기반 에이전트를 구축하는 ML 엔지니어, 프로토타입을 프로덕션으로 전환하는 AI 팀, 자체 환경에서 실행할 수 있는 오픈 소스 자체 호스팅 관측성이 필요한 엔지니어링 팀입니다.

> **오픈 소스가 중요한 이유:** Opik은 Apache-2.0 라이선스로, 클라이언트 SDK뿐 아니라 백엔드를 포함한 전체 플랫폼을 무료로 자체 호스팅할 수 있습니다. 이 저장소에는 서버 백엔드, 웹 애플리케이션, 추적, 데이터셋, 실험, 평가, 프롬프트 관리, 온라인 평가 및 에이전트 최적화 구성 요소가 모두 Apache-2.0 라이선스로 포함되어 있습니다. 데이터가 환경 밖으로 나가지 않도록 자체 인프라에서 LLM 관측성을 운영할 수 있으며 Enterprise 영업 상담도 필요하지 않습니다.

> [!TIP]
> 현재 Opik에 없는 기능이 필요하다면 새 [기능 요청](https://github.com/comet-ml/opik/issues/new/choose)을 등록해 주세요 🚀

<br>

<a id="-quick-start"></a>
## ⚡ 빠른 시작

Python SDK를 설치하고 구성합니다.

```bash
pip install opik
opik configure
```

아무 함수에나 `@track` 데코레이터를 적용하면 트레이스 기록이 시작됩니다.

```python
from opik import track

@track
def my_function(input: str) -> str:
    return input
```

이제 중첩 호출을 포함한 `my_function`의 모든 호출이 Opik에 기록되므로 단일 LLM 호출뿐 아니라 전체 에이전트와 파이프라인 트레이스에도 사용할 수 있습니다. TypeScript SDK와 다른 설정 방법은 [빠른 시작 가이드](https://www.comet.com/docs/opik/quickstart?from=llm&utm_source=opik&utm_medium=github&utm_content=quickstart_hero_link&utm_campaign=opik)를 참고하세요.

### 코딩 에이전트 연결

Claude Code, Cursor, VS Code Copilot, Codex 또는 opencode가 채팅에서 트레이스를 읽고, 출력에 점수를 매기고, 평가를 실행하게 하세요. 명령어 하나로 설정할 수 있습니다. [`uv`](https://docs.astral.sh/uv/)가 필요하며 SDK는 필요하지 않습니다.

```bash
uvx opik mcp configure
```

[![Add to Cursor](https://cursor.com/deeplink/mcp-install-dark.svg)](https://cursor.com/en/install-mcp?name=opik-mcp&config=eyJ1cmwiOiJodHRwczovL3d3dy5jb21ldC5jb20vb3Bpay9hcGkvdjEvbWNwIn0%3D)
[![Install in VS Code](https://img.shields.io/badge/VS_Code-Install_Server-0098FF?style=flat-square&logo=visualstudiocode&logoColor=white)](https://insiders.vscode.dev/redirect/mcp/install?name=opik-mcp&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fwww.comet.com%2Fopik%2Fapi%2Fv1%2Fmcp%22%7D)

아래 배지와 `add-mcp` 대체 명령은 Opik Cloud용이며, 위 명령은 자체 호스팅 배포도 지원합니다. Opik Cloud의 다른 MCP 클라이언트에서는 `npx add-mcp https://www.comet.com/opik/api/v1/mcp --name opik-mcp`를 사용하세요. 자세한 내용, 문제 해결 방법 및 자주 묻는 질문은 [MCP 서버 가이드](https://www.comet.com/docs/opik/mcp-server?utm_source=opik&utm_medium=github&utm_content=mcp_quickstart_link&utm_campaign=opik)에 있습니다.

<br>

<a id="-how-opik-compares"></a>
## 📊 Opik 비교

Opik은 **LangSmith, Arize(Phoenix 및 Arize AX), Weights & Biases(Weave), Langfuse, Braintrust**와 함께 **LLM 관측성/AI 에이전트 평가** 분야에서 경쟁합니다.

| 기능 | Opik | LangSmith | Phoenix | Arize AX | Weights & Biases (Weave) | Langfuse | Braintrust |
|---|---|---|---|---|---|---|---|
| 오픈 소스 | 예, Apache-2.0(전체 플랫폼) | 아니요 | 소스 공개(Elastic License 2.0, OSI 미승인) | 아니요 | 오픈 소스 SDK/도구 모음, 자체 관리 플랫폼에는 상용 라이선스 필요 | MIT 라이선스 핵심 플랫폼, 상용 엔터프라이즈 모듈 | 아니요 |
| 자체 호스팅 배포 | 예 | Enterprise 전용 | 예 | Enterprise 전용 | Weave 자체는 Enterprise 전용 | 예, 핵심 기능 | Enterprise 전용 |
| 무료 등급 제공(클라우드 또는 자체 호스팅) | 둘 다 | 예, 클라우드 | 예, 자체 호스팅 | 예, 클라우드 | 예, 클라우드 | 둘 다 | 예, 클라우드 |
| 에이전트/다단계 추적 | 예 | 예 | 예 | 예 | 예 | 예 | 예 |
| LLM 심사 평가 | 예 | 예 | 예 | 예 | 예 | 예 | 예 |
| 프롬프트 관리 | 예 | 예 | 일부 | 일부 | 일부 | 예 | 예 |
| 프레임워크 독립적 | 예 | 일부, LangChain 중심 | 예 | 예 | 예 | 예 | 예 |

**팀이 Opik을 선택하는 이유:** Opik의 전체 관측성, 평가 및 최적화 플랫폼은 Apache-2.0 라이선스로 무료 자체 호스팅이 가능합니다. 자체 호스팅 배포에 Enterprise 요금제가 필요한 폐쇄형 플랫폼과 달리 상용 라이선스 없이 배포할 수 있으며, 프레임워크에 독립적이어서 하나의 에이전트 생태계에 종속되지 않습니다. 대안별 자체 호스팅과 라이선스의 차이는 위 표를 참고하세요.

<br>

<a id="-frequently-asked-questions"></a>
## ❓ 자주 묻는 질문

#### Opik은 오픈 소스인가요?
Opik은 Apache 2.0 라이선스로 제공됩니다. 서버, 웹 애플리케이션 및 핵심 관측성·평가 기능을 상용 라이선스 없이 자체 호스팅할 수 있습니다.

#### Opik을 자체 호스팅할 수 있나요?
예. 문서에 안내된 자체 호스팅 옵션을 사용해 로컬 또는 자체 인프라에 Opik을 배포할 수 있습니다.

#### Opik은 AI 에이전트 추적을 지원하나요?
예. Opik은 LLM 호출, 도구 실행, 검색 단계 및 기타 에이전트 활동이 포함된 다단계 트레이스를 수집합니다.

#### Opik은 LLM 평가를 지원하나요?
예. Opik은 데이터셋, 실험, 코드 기반 지표, LLM 심사 평가 및 온라인 평가를 지원합니다.

#### Opik은 특정 에이전트 프레임워크에 종속되나요?
아니요. Opik은 프레임워크에 독립적이며 자체 SDK, OpenTelemetry 및 프레임워크별 통합을 지원합니다.

<br>

<a id="%EF%B8%8F-opik-server-installation"></a>
## 🛠️ Opik 서버 설치

몇 분 안에 Opik 서버를 실행할 수 있습니다. 필요에 가장 적합한 옵션을 선택하세요.

### 옵션 1: Comet.com Cloud(가장 쉽고 권장)

설정 없이 Opik을 즉시 사용하세요. 빠른 시작과 간편한 유지 관리에 적합합니다.

👉 [무료 Comet 계정 만들기](https://www.comet.com/signup?from=llm&utm_source=opik&utm_medium=github&utm_content=install_create_link&utm_campaign=opik)

### 옵션 2: 완전한 제어를 위한 Opik 자체 호스팅

자체 환경에 Opik을 배포합니다. 로컬 설정에는 Docker를, 확장성이 필요할 때는 Kubernetes를 선택하세요.

#### Docker Compose로 자체 호스팅(로컬 개발 및 테스트용)

로컬 Opik 인스턴스를 실행하는 가장 간단한 방법입니다. 새로운 `./opik.sh` 설치 스크립트를 사용합니다.

Linux 또는 Mac 환경:

```bash
# Opik 저장소 복제
git clone https://github.com/comet-ml/opik.git

# 저장소로 이동
cd opik

# Opik 플랫폼 시작
./opik.sh
```

Windows 환경:

```powershell
# Opik 저장소 복제
git clone https://github.com/comet-ml/opik.git

# 저장소로 이동
cd opik

# Opik 플랫폼 시작
powershell -ExecutionPolicy ByPass -c ".\\opik.ps1"
```

**설치 스크립트 옵션**

`opik.sh` 및 `opik.ps1` 스크립트는 다음 옵션을 지원합니다.

```bash
# 전체 Opik 제품군 시작(기본 동작)
./opik.sh

# 인프라 서비스만 시작(데이터베이스, 캐시 등)
./opik.sh --infra

# 인프라 및 백엔드 서비스 시작
./opik.sh --backend

# 모든 프로필에서 Guardrails 활성화
./opik.sh --guardrails # 전체 Opik 제품군에서 Guardrails 사용
./opik.sh --backend --guardrails # 인프라 및 백엔드에서 Guardrails 사용

# 시작하기 전에 소스에서 컨테이너 빌드
./opik.sh --build

# 모든 컨테이너의 상태 확인
./opik.sh --verify

# 모든 컨테이너 중지
./opik.sh --stop

# 모든 컨테이너를 중지하고 Opik 데이터 볼륨 모두 제거
# 경고: 모든 OPIK 데이터가 삭제됩니다
./opik.sh --clean

# 사용 가능한 모든 옵션 표시
./opik.sh --help
```

문제를 해결하려면 `--help` 또는 `--info` 옵션을 사용하세요. 보안 강화를 위해 Dockerfile은 컨테이너가 루트가 아닌 사용자로 실행되도록 보장합니다. 모든 서비스가 실행되면 브라우저에서 [localhost:5173](http://localhost:5173)에 접속할 수 있습니다. 자세한 내용은 [로컬 배포 가이드](https://www.comet.com/docs/opik/self-host/local_deployment?from=llm&utm_source=opik&utm_medium=github&utm_content=self_host_link&utm_campaign=opik)를 참고하세요.

#### Kubernetes 및 Helm으로 자체 호스팅(확장 가능한 배포용)

프로덕션 또는 대규모 자체 호스팅 배포에서는 Helm 차트를 사용해 Kubernetes 클러스터에 Opik을 설치할 수 있습니다. 배지를 클릭해 전체 [Helm 기반 Kubernetes 설치 가이드](https://www.comet.com/docs/opik/self-host/kubernetes/#kubernetes-installation?from=llm&utm_source=opik&utm_medium=github&utm_content=kubernetes_link&utm_campaign=opik)를 확인하세요.

[![Kubernetes](https://img.shields.io/badge/Kubernetes-%23326ce5.svg?&logo=kubernetes&logoColor=white)](https://www.comet.com/docs/opik/self-host/kubernetes/#kubernetes-installation?from=llm&utm_source=opik&utm_medium=github&utm_content=kubernetes_link&utm_campaign=opik)

<a id="-opik-client-sdk"></a>
## 💻 Opik 클라이언트 SDK

Opik은 Opik 서버와 상호 작용하는 클라이언트 라이브러리 모음과 REST API를 제공합니다. Python 및 TypeScript SDK와 공식 [OpenTelemetry](https://www.comet.com/docs/opik/tracing/opentelemetry/overview?from=llm&utm_source=opik&utm_medium=github&utm_content=otel_link&utm_campaign=opik) 지원이 포함됩니다. [Java](https://www.comet.com/docs/opik/integrations/spring-ai?from=llm&utm_source=opik&utm_medium=github&utm_content=java_link&utm_campaign=opik), [Ruby](https://www.comet.com/docs/opik/integrations/opentelemetry-ruby-sdk?from=llm&utm_source=opik&utm_medium=github&utm_content=ruby_link&utm_campaign=opik), .NET 등 OpenTelemetry SDK가 있는 모든 언어에서 Opik으로 트레이스를 전송할 수 있습니다. 자세한 API 및 SDK 레퍼런스는 [Opik 클라이언트 레퍼런스 문서](https://www.comet.com/docs/opik/reference/overview?from=llm&utm_source=opik&utm_medium=github&utm_content=reference_link&utm_campaign=opik)를 참고하세요.

### Python SDK 빠른 시작

Python SDK를 시작하려면 다음 단계를 따르세요.

패키지를 설치합니다.

```bash
# pip로 설치
pip install opik

# 또는 uv로 설치
uv pip install opik
```

`opik configure` 명령을 실행해 Python SDK를 구성합니다. 자체 호스팅 인스턴스의 Opik 서버 주소 또는 Comet.com의 API 키와 워크스페이스를 입력하라는 메시지가 표시됩니다.

```bash
opik configure
```

> [!TIP]
> Python 코드에서 `opik.configure(use_local=True)`를 호출해 SDK가 로컬 자체 호스팅 설치에서 실행되도록 구성할 수도 있고, Comet.com API 키와 워크스페이스 정보를 직접 제공할 수도 있습니다. 더 많은 구성 옵션은 [Python SDK 문서](https://www.comet.com/docs/opik/python-sdk-reference/?from=llm&utm_source=opik&utm_medium=github&utm_content=python_sdk_docs_link&utm_campaign=opik)를 참고하세요.

이제 [Python SDK](https://www.comet.com/docs/opik/python-sdk-reference/?from=llm&utm_source=opik&utm_medium=github&utm_content=sdk_link2&utm_campaign=opik)를 사용해 트레이스를 기록할 준비가 되었습니다.

<a id="-logging-traces-with-integrations"></a>
### 📝 통합으로 트레이스 기록

트레이스를 기록하는 가장 쉬운 방법은 직접 통합 중 하나를 사용하는 것입니다. Opik은 최근 추가된 **Google ADK**, **Autogen**, **AG2**, **Flowise AI**를 비롯해 다양한 프레임워크를 지원합니다.

| 통합 | 설명 | 문서 |
| --------------------- | ------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| ADK                   | ADK 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/adk?utm_source=opik&utm_medium=github&utm_content=google_adk_link&utm_campaign=opik)                              |
| AG2                   | AG2 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/ag2?utm_source=opik&utm_medium=github&utm_content=ag2_link&utm_campaign=opik)                                     |
| Agent Spec            | Agent Spec 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/agentspec?utm_source=opik&utm_medium=github&utm_content=agentspec_link&utm_campaign=opik)                         |
| AIsuite               | AIsuite 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/aisuite?utm_source=opik&utm_medium=github&utm_content=aisuite_link&utm_campaign=opik)                             |
| Agno                  | Agno 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/agno?utm_source=opik&utm_medium=github&utm_content=agno_link&utm_campaign=opik)                                   |
| Anthropic             | Anthropic 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/anthropic?utm_source=opik&utm_medium=github&utm_content=anthropic_link&utm_campaign=opik)                         |
| Autogen               | Autogen 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/autogen?utm_source=opik&utm_medium=github&utm_content=autogen_link&utm_campaign=opik)                             |
| Bedrock               | Bedrock 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/bedrock?utm_source=opik&utm_medium=github&utm_content=bedrock_link&utm_campaign=opik)                             |
| BeeAI (Python)        | BeeAI (Python) 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/beeai?utm_source=opik&utm_medium=github&utm_content=beeai_link&utm_campaign=opik)                                 |
| BeeAI (TypeScript)    | BeeAI (TypeScript) 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/beeai-typescript?utm_source=opik&utm_medium=github&utm_content=beeai_typescript_link&utm_campaign=opik)           |
| BytePlus              | BytePlus 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/byteplus?utm_source=opik&utm_medium=github&utm_content=byteplus_link&utm_campaign=opik)                           |
| Claude Code           | Opik 플러그인을 통한 Claude Code 세션 트레이스 기록 | [GitHub](https://github.com/comet-ml/opik-claude-code-plugin)                                                                                                                 |
| Cloudflare Workers AI | Cloudflare Workers AI 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/cloudflare-workers-ai?utm_source=opik&utm_medium=github&utm_content=cloudflare_workers_ai_link&utm_campaign=opik) |
| Cohere                | Cohere 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/cohere?utm_source=opik&utm_medium=github&utm_content=cohere_link&utm_campaign=opik)                               |
| CrewAI                | CrewAI 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/crewai?utm_source=opik&utm_medium=github&utm_content=crewai_link&utm_campaign=opik)                               |
| Cursor                | Cursor 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/cursor?utm_source=opik&utm_medium=github&utm_content=cursor_link&utm_campaign=opik)                               |
| DeepSeek              | DeepSeek 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/deepseek?utm_source=opik&utm_medium=github&utm_content=deepseek_link&utm_campaign=opik)                           |
| Dify                  | Dify 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/dify?utm_source=opik&utm_medium=github&utm_content=dify_link&utm_campaign=opik)                                   |
| DSPY                  | DSPY 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/dspy?utm_source=opik&utm_medium=github&utm_content=dspy_link&utm_campaign=opik)                                   |
| Fireworks AI          | Fireworks AI 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/fireworks-ai?utm_source=opik&utm_medium=github&utm_content=fireworks_ai_link&utm_campaign=opik)                   |
| Flowise AI            | Flowise AI 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/flowise?utm_source=opik&utm_medium=github&utm_content=flowise_link&utm_campaign=opik)                             |
| Gemini (Python)       | Gemini (Python) 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/gemini?utm_source=opik&utm_medium=github&utm_content=gemini_link&utm_campaign=opik)                               |
| Gemini (TypeScript)   | Gemini (TypeScript) 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/gemini-typescript?utm_source=opik&utm_medium=github&utm_content=gemini_typescript_link&utm_campaign=opik)         |
| Groq                  | Groq 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/groq?utm_source=opik&utm_medium=github&utm_content=groq_link&utm_campaign=opik)                                   |
| Guardrails            | Guardrails 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/guardrails-ai?utm_source=opik&utm_medium=github&utm_content=guardrails_link&utm_campaign=opik)                    |
| Haystack              | Haystack 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/haystack?utm_source=opik&utm_medium=github&utm_content=haystack_link&utm_campaign=opik)                           |
| Harbor                | Harbor 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/harbor?utm_source=opik&utm_medium=github&utm_content=harbor_link&utm_campaign=opik)                               |
| Instructor            | Instructor 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/instructor?utm_source=opik&utm_medium=github&utm_content=instructor_link&utm_campaign=opik)                       |
| LangChain (Python)    | LangChain (Python) 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/langchain?utm_source=opik&utm_medium=github&utm_content=langchain_link&utm_campaign=opik)                         |
| LangChain (JS/TS)     | LangChain (JS/TS) 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/langchainjs?utm_source=opik&utm_medium=github&utm_content=langchainjs_link&utm_campaign=opik)                     |
| LangGraph             | LangGraph 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/langgraph?utm_source=opik&utm_medium=github&utm_content=langgraph_link&utm_campaign=opik)                         |
| Langflow              | Langflow 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/langflow?utm_source=opik&utm_medium=github&utm_content=langflow_link&utm_campaign=opik)                           |
| LiteLLM               | LiteLLM 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/litellm?utm_source=opik&utm_medium=github&utm_content=litellm_link&utm_campaign=opik)                             |
| LiveKit Agents        | LiveKit Agents 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/livekit?utm_source=opik&utm_medium=github&utm_content=livekit_link&utm_campaign=opik)                             |
| LlamaIndex            | LlamaIndex 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/llama_index?utm_source=opik&utm_medium=github&utm_content=llama_index_link&utm_campaign=opik)                     |
| Mastra                | Mastra 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/mastra?utm_source=opik&utm_medium=github&utm_content=mastra_link&utm_campaign=opik)                               |
| MCP Server (opik-mcp) | Claude Code, Cursor 또는 VS Code에서 Model Context Protocol을 통해 Opik 제어 | [문서](https://www.comet.com/docs/opik/integrations/mcp-server?utm_source=opik&utm_medium=github&utm_content=mcp_server_link&utm_campaign=opik) |
| Microsoft Agent Framework (Python) | Microsoft Agent Framework (Python) 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/microsoft-agent-framework?utm_source=opik&utm_medium=github&utm_content=agent_framework_link&utm_campaign=opik)              |
| Microsoft Agent Framework (.NET) | Microsoft Agent Framework (.NET) 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/microsoft-agent-framework-dotnet?utm_source=opik&utm_medium=github&utm_content=agent_framework_dotnet_link&utm_campaign=opik) |
| Mistral AI            | Mistral AI 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/mistral?utm_source=opik&utm_medium=github&utm_content=mistral_link&utm_campaign=opik)                             |
| n8n                   | n8n 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/n8n?utm_source=opik&utm_medium=github&utm_content=n8n_link&utm_campaign=opik)                                     |
| Novita AI             | Novita AI 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/novita-ai?utm_source=opik&utm_medium=github&utm_content=novita_ai_link&utm_campaign=opik)                         |
| Ollama                | Ollama 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/ollama?utm_source=opik&utm_medium=github&utm_content=ollama_link&utm_campaign=opik)                               |
| OpenAI (Python)       | OpenAI (Python) 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/openai?utm_source=opik&utm_medium=github&utm_content=openai_link&utm_campaign=opik)                               |
| OpenAI (JS/TS)        | OpenAI (JS/TS) 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/openai-typescript?utm_source=opik&utm_medium=github&utm_content=openai_typescript_link&utm_campaign=opik)         |
| OpenAI Agents         | OpenAI Agents 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/openai_agents?utm_source=opik&utm_medium=github&utm_content=openai_agents_link&utm_campaign=opik)                 |
| OpenClaw              | OpenClaw 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/openclaw?utm_source=opik&utm_medium=github&utm_content=openclaw_link&utm_campaign=opik) |
| OpenRouter            | OpenRouter 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/openrouter?utm_source=opik&utm_medium=github&utm_content=openrouter_link&utm_campaign=opik)                       |
| OpenTelemetry         | OpenTelemetry 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/tracing/opentelemetry/overview?utm_source=opik&utm_medium=github&utm_content=opentelemetry_link&utm_campaign=opik)             |
| OpenWebUI             | OpenWebUI 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/openwebui?utm_source=opik&utm_medium=github&utm_content=openwebui_link&utm_campaign=opik)                         |
| Pipecat               | Pipecat 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/pipecat?utm_source=opik&utm_medium=github&utm_content=pipecat_link&utm_campaign=opik)                             |
| Predibase             | Predibase 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/predibase?utm_source=opik&utm_medium=github&utm_content=predibase_link&utm_campaign=opik)                         |
| Pydantic AI           | Pydantic AI 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/pydantic-ai?utm_source=opik&utm_medium=github&utm_content=pydantic_ai_link&utm_campaign=opik)                     |
| Ragas                 | Ragas 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/ragas?utm_source=opik&utm_medium=github&utm_content=ragas_link&utm_campaign=opik)                                 |
| Semantic Kernel       | Semantic Kernel 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/semantic-kernel?utm_source=opik&utm_medium=github&utm_content=semantic_kernel_link&utm_campaign=opik)             |
| Smolagents            | Smolagents 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/smolagents?utm_source=opik&utm_medium=github&utm_content=smolagents_link&utm_campaign=opik)                       |
| Spring AI             | Spring AI 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/spring-ai?utm_source=opik&utm_medium=github&utm_content=spring_ai_link&utm_campaign=opik)                         |
| Strands Agents        | Strands Agents 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/strands-agents?utm_source=opik&utm_medium=github&utm_content=strands_agents_link&utm_campaign=opik)               |
| Together AI           | Together AI 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/together-ai?utm_source=opik&utm_medium=github&utm_content=together_ai_link&utm_campaign=opik)                     |
| TrueFoundry           | TrueFoundry 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/truefoundry?utm_source=opik&utm_medium=github&utm_content=truefoundry_link&utm_campaign=opik)                     |
| TypeSafe AI           | TypeSafe AI 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/typesafe?utm_source=opik&utm_medium=github&utm_content=typesafe_link&utm_campaign=opik)                           |
| Vercel AI SDK         | Vercel AI SDK 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/vercel-ai-sdk?utm_source=opik&utm_medium=github&utm_content=vercel_ai_sdk_link&utm_campaign=opik)                 |
| VoltAgent             | VoltAgent 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/voltagent?utm_source=opik&utm_medium=github&utm_content=voltagent_link&utm_campaign=opik)                         |
| WatsonX               | WatsonX 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/watsonx?utm_source=opik&utm_medium=github&utm_content=watsonx_link&utm_campaign=opik)                             |
| xAI Grok              | xAI Grok 호출 및 실행 트레이스 기록 | [문서](https://www.comet.com/docs/opik/integrations/xai-grok?utm_source=opik&utm_medium=github&utm_content=xai_grok_link&utm_campaign=opik)                           |

> [!TIP]
> 사용하는 프레임워크가 위에 없다면 언제든 [이슈를 등록](https://github.com/comet-ml/opik/issues)하거나 해당 통합을 PR로 제출해 주세요.

위 프레임워크를 사용하지 않는 경우에도 `track` 함수 데코레이터를 사용해 [트레이스를 기록](https://www.comet.com/docs/opik/tracing/advanced/log_traces/?from=llm&utm_source=opik&utm_medium=github&utm_content=traces_link&utm_campaign=opik)할 수 있습니다.

```python
import opik

opik.configure(use_local=True) # 로컬에서 실행

@opik.track
def my_llm_function(user_question: str) -> str:
    # 여기에 LLM 코드 작성

    return "Hello"
```

> [!TIP]
> track 데코레이터는 모든 통합과 함께 사용할 수 있으며 중첩된 함수 호출도 추적할 수 있습니다.

<a id="-llm-as-a-judge-metrics"></a>
### 🧑‍⚖️ LLM 심사 지표

Python Opik SDK에는 LLM 애플리케이션 평가에 도움이 되는 여러 LLM 심사 지표가 포함되어 있습니다. 자세한 내용은 [지표 문서](https://www.comet.com/docs/opik/evaluation/metrics/overview/?from=llm&utm_source=opik&utm_medium=github&utm_content=metrics_2_link&utm_campaign=opik)를 참고하세요.

사용하려면 관련 지표를 가져와 `score` 함수를 호출하면 됩니다.

```python
from opik.evaluation.metrics import Hallucination

metric = Hallucination()
score = metric.score(
    input="What is the capital of France?",
    output="Paris",
    context=["France is a country in Europe."]
)
print(score)
```

Opik에는 미리 만들어진 여러 휴리스틱 지표가 포함되어 있으며 직접 만들 수도 있습니다. 자세한 내용은 [지표 문서](https://www.comet.com/docs/opik/evaluation/metrics/overview?from=llm&utm_source=opik&utm_medium=github&utm_content=metrics_3_link&utm_campaign=opik)를 참고하세요.

<a id="-evaluating-your-llm-application"></a>
### 🔍 LLM 애플리케이션 평가

Opik에서는 [데이터셋](https://www.comet.com/docs/opik/evaluation/advanced/manage_datasets/?from=llm&utm_source=opik&utm_medium=github&utm_content=datasets_2_link&utm_campaign=opik)과 [실험](https://www.comet.com/docs/opik/evaluation/advanced/evaluate_your_llm/?from=llm&utm_source=opik&utm_medium=github&utm_content=experiments_link&utm_campaign=opik)을 통해 개발 중 LLM 애플리케이션을 평가할 수 있습니다. Opik 대시보드는 향상된 실험 차트와 대규모 트레이스 처리 기능을 제공합니다. 또한 [PyTest 통합](https://www.comet.com/docs/opik/evaluation/overview/?from=llm&utm_source=opik&utm_medium=github&utm_content=pytest_2_link&utm_campaign=opik)을 사용해 CI/CD 파이프라인의 일부로 평가를 실행할 수 있습니다.

<a id="-star-us-on-github"></a>
## ⭐ GitHub에서 스타 남기기

Opik이 유용하다면 스타를 남겨 주세요! 여러분의 응원은 커뮤니티를 성장시키고 제품을 계속 개선하는 데 도움이 됩니다.

<a href="https://github.com/comet-ml/opik">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://cdn.comet.com/opik/star-history/star-history-dark.svg" />
    <img alt="스타 기록 차트" src="https://cdn.comet.com/opik/star-history/star-history-light.svg" />
  </picture>
</a>

<a id="-contributing"></a>
## 🤝 기여하기

Opik에 기여하는 방법은 다양합니다.

- [버그 보고](https://github.com/comet-ml/opik/issues) 및 [기능 요청](https://github.com/comet-ml/opik/issues) 제출
- 문서를 검토하고 개선을 위한 [Pull Request](https://github.com/comet-ml/opik/pulls) 제출
- Opik에 관해 발표하거나 글을 쓰고 [알려 주기](https://chat.comet.com)
- [인기 기능 요청](https://github.com/comet-ml/opik/issues?q=is%3Aissue+is%3Aopen+label%3A%22enhancement%22)에 투표해 지지 표시

Opik 기여 방법에 관한 자세한 내용은 [기여 가이드](CONTRIBUTING.md)를 참고하세요.
