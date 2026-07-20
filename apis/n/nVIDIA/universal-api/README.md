# <img src="https://images.mindcloud.co/apps/icons/nvidia-logo_1776123030676.png" alt="NVIDIA logo" width="28" height="28"> NVIDIA: Universal API

NVIDIA NIM LLM APIs and model response endpoints.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/nVIDIA/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.nvidia.com/
- **Vendor API docs:** https://docs.api.nvidia.com/nim/reference/llm-apis

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Models](actions/list-models.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nVIDIA/latest/actions/list-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Abacusai/dracarys-llama-3.1-70b-instruct

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat Completion (abacusai/dracarys-llama-3.1-70b-instruct)](actions/create-chat-completion-abacusai-dracarys-llama-3-1-70b-instruct.md) | POST | Creates a chat completion in NVIDIA using abacusai/dracarys-llama-3.1-70b-instruct. |

### Aisingapore/sea-lion-7b-instruct

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat Completion (aisingapore/sea-lion-7b-instruct)](actions/create-chat-completion-aisingapore-sea-lion-7b-instruct.md) | POST | Creates a chat completion in NVIDIA using aisingapore/sea-lion-7b-instruct. |

### Baichuan-inc/baichuan2-13b-chat

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat Completion (baichuan-inc/baichuan2-13b-chat)](actions/create-chat-completion-baichuan-inc-baichuan2-13b-chat.md) | POST | Creates a chat completion in NVIDIA using baichuan-inc/baichuan2-13b-chat. |

### Bytedance/seed-oss-36b-instruct

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat Completion (bytedance/seed-oss-36b-instruct)](actions/create-chat-completion-bytedance-seed-oss-36b-instruct.md) | POST | Creates a chat completion in NVIDIA using bytedance/seed-oss-36b-instruct. |

### Deepseek-ai/deepseek-r1-distill-llama-8b

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat Completion (deepseek-ai/deepseek-r1-distill-llama-8b)](actions/create-chat-completion-deepseek-ai-deepseek-r1-distill-llama-8b.md) | POST | Creates a chat completion in NVIDIA using deepseek-ai/deepseek-r1-distill-llama-8b. |

### Deepseek-ai/deepseek-r1-distill-qwen-14b

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat Completion (deepseek-ai/deepseek-r1-distill-qwen-14b)](actions/create-chat-completion-deepseek-ai-deepseek-r1-distill-qwen-14b.md) | POST | Creates a chat completion in NVIDIA using deepseek-ai/deepseek-r1-distill-qwen-14b. |

### Deepseek-ai/deepseek-r1-distill-qwen-32b

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat Completion (deepseek-ai/deepseek-r1-distill-qwen-32b)](actions/create-chat-completion-deepseek-ai-deepseek-r1-distill-qwen-32b.md) | POST | Creates a chat completion in NVIDIA using deepseek-ai/deepseek-r1-distill-qwen-32b. |

### Deepseek-ai/deepseek-r1-distill-qwen-7b

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat Completion (deepseek-ai/deepseek-r1-distill-qwen-7b)](actions/create-chat-completion-deepseek-ai-deepseek-r1-distill-qwen-7b.md) | POST | Creates a chat completion in NVIDIA using deepseek-ai/deepseek-r1-distill-qwen-7b. |

### Deepseek-ai/deepseek-v3.1

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat Completion (deepseek-ai/deepseek-v3.1)](actions/create-chat-completion-deepseek-ai-deepseek-v3-1.md) | POST | Creates a chat completion in NVIDIA using deepseek-ai/deepseek-v3.1. |

### Deepseek-ai/deepseek-v3.1-terminus

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat Completion (deepseek-ai/deepseek-v3.1-terminus)](actions/create-chat-completion-deepseek-ai-deepseek-v3-1-terminus.md) | POST | Creates a chat completion in NVIDIA using deepseek-ai/deepseek-v3.1-terminus. |

### Deepseek-ai/deepseek-v3.2

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat Completion (deepseek-ai/deepseek-v3.2)](actions/create-chat-completion-deepseek-ai-deepseek-v3-2.md) | POST | Creates a chat completion in NVIDIA using deepseek-ai/deepseek-v3.2. |

### Google/gemma-2-27b-it

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat Completion (google/gemma-2-27b-it)](actions/create-chat-completion-google-gemma-2-27b-it.md) | POST | Creates a chat completion in NVIDIA using google/gemma-2-27b-it. |

### Google/gemma-2-2b-it

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat Completion (google/gemma-2-2b-it)](actions/create-chat-completion-google-gemma-2-2b-it.md) | POST | Creates a chat completion in NVIDIA using google/gemma-2-2b-it. |

### Google/gemma-2-9b-it

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat Completion (google/gemma-2-9b-it)](actions/create-chat-completion-google-gemma-2-9b-it.md) | POST | Creates a chat completion in NVIDIA using google/gemma-2-9b-it. |

### Google/gemma-3-1b-it

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat Completion (google/gemma-3-1b-it)](actions/create-chat-completion-google-gemma-3-1b-it.md) | POST | Creates a chat completion in NVIDIA using google/gemma-3-1b-it. |

### Google/gemma-7b

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat Completion (google/gemma-7b)](actions/create-chat-completion-google-gemma-7b.md) | POST | Creates a chat completion in NVIDIA using google/gemma-7b. |

### Google/shieldgemma-9b

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat Completion (google/shieldgemma-9b)](actions/create-chat-completion-google-shieldgemma-9b.md) | POST | Creates a chat completion in NVIDIA using google/shieldgemma-9b. |

### Ibm/granite-3_3-8b-instruct

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat Completion (ibm/granite-3_3-8b-instruct)](actions/create-chat-completion-ibm-granite-3-3-8b-instruct.md) | POST | Creates a chat completion in NVIDIA using ibm/granite-3_3-8b-instruct. |

### Ibm/granite-guardian-3.0-8b

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat Completion (ibm/granite-guardian-3.0-8b)](actions/create-chat-completion-ibm-granite-guardian-3-0-8b.md) | POST | Creates a chat completion in NVIDIA using ibm/granite-guardian-3.0-8b. |

### Igenius/colosseum_355b_instruct_16k

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat Completion (igenius/colosseum_355b_instruct_16k)](actions/create-chat-completion-igenius-colosseum-355b-instruct-16k.md) | POST | Creates a chat completion in NVIDIA using igenius/colosseum_355b_instruct_16k. |

### Institute-of-science-tokyo/llama-3.1-swallow-70b-instruct-v01

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat Completion (institute-of-science-tokyo/llama-3.1-swallow-70b-instruct-v01)](actions/create-chat-completion-institute-of-science-tokyo-llama-3-1-swallow-70b-instruct-v01.md) | POST | Creates a chat completion in NVIDIA using institute-of-science-tokyo/llama-3.1-swallow-70b-instruct-v01. |

### Marin/marin-8b-instruct

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat Completion (marin/marin-8b-instruct)](actions/create-chat-completion-marin-marin-8b-instruct.md) | POST | Creates a chat completion in NVIDIA using marin/marin-8b-instruct. |

### Meta/llama3-8b-instruct

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat Completion (meta/llama3-8b-instruct)](actions/create-chat-completion-meta-llama3-8b-instruct.md) | POST | Creates a chat completion in NVIDIA using meta/llama3-8b-instruct. |

### Microsoft/phi-3-medium-128k-instruct

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat Completion (microsoft/phi-3-medium-128k-instruct)](actions/create-chat-completion-microsoft-phi-3-medium-128k-instruct.md) | POST | Creates a chat completion in NVIDIA using microsoft/phi-3-medium-128k-instruct. |

### Microsoft/phi-3-mini-128k-instruct

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat Completion (microsoft/phi-3-mini-128k-instruct)](actions/create-chat-completion-microsoft-phi-3-mini-128k-instruct.md) | POST | Creates a chat completion in NVIDIA using microsoft/phi-3-mini-128k-instruct. |

### Mistralai/mistral-7b-instruct

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat Completion (mistralai/mistral-7b-instruct)](actions/create-chat-completion-mistralai-mistral-7b-instruct.md) | POST | Creates a chat completion in NVIDIA using mistralai/mistral-7b-instruct. |

### Mistralai/mistral-large-2-instruct

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat Completion (mistralai/mistral-large-2-instruct)](actions/create-chat-completion-mistralai-mistral-large-2-instruct.md) | POST | Creates a chat completion in NVIDIA using mistralai/mistral-large-2-instruct. |

### Models

| Action | Method | Description |
| --- | --- | --- |
| [List Models](actions/list-models.md) | GET | Retrieves available models from NVIDIA. |

### Nvidia/llama3-chatqa-1.5-70b

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat Completion (nvidia/llama3-chatqa-1.5-70b)](actions/create-chat-completion-nvidia-llama3-chatqa-1-5-70b.md) | POST | Creates a chat completion in NVIDIA using nvidia/llama3-chatqa-1.5-70b. |

### Nvidia/nemotron-4-340b-instruct

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat Completion (nvidia/nemotron-4-340b-instruct)](actions/create-chat-completion-nvidia-nemotron-4-340b-instruct.md) | POST | Creates a chat completion in NVIDIA using nvidia/nemotron-4-340b-instruct. |

### Nvidia/nemotron-4-340b-reward

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat Completion (nvidia/nemotron-4-340b-reward)](actions/create-chat-completion-nvidia-nemotron-4-340b-reward.md) | POST | Creates a chat completion in NVIDIA using nvidia/nemotron-4-340b-reward. |

