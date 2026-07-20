# NVIDIA: Native API Reference

A consolidated summary of NVIDIA's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://docs.api.nvidia.com/nim/reference/llm-apis
- **API base URL:** `https://integrate.api.nvidia.com`

## Authentication

### NVIDIA API Key

Use an NVIDIA API key from build.nvidia.com.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://build.nvidia.com/settings/api-keys)

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Chat Completion (abacusai/dracarys-llama-3.1-70b-instruct)](actions/create-chat-completion-abacusai-dracarys-llama-3-1-70b-instruct.md) | `POST /v1/chat/completions` | [docs](https://docs.api.nvidia.com/nim/reference/llm-apis) |
| [Create Chat Completion (aisingapore/sea-lion-7b-instruct)](actions/create-chat-completion-aisingapore-sea-lion-7b-instruct.md) | `POST /v1/chat/completions` | [docs](https://docs.api.nvidia.com/nim/reference/llm-apis) |
| [Create Chat Completion (baichuan-inc/baichuan2-13b-chat)](actions/create-chat-completion-baichuan-inc-baichuan2-13b-chat.md) | `POST /v1/chat/completions` | [docs](https://docs.api.nvidia.com/nim/reference/llm-apis) |
| [Create Chat Completion (bytedance/seed-oss-36b-instruct)](actions/create-chat-completion-bytedance-seed-oss-36b-instruct.md) | `POST /v1/chat/completions` | [docs](https://docs.api.nvidia.com/nim/reference/llm-apis) |
| [Create Chat Completion (deepseek-ai/deepseek-r1-distill-llama-8b)](actions/create-chat-completion-deepseek-ai-deepseek-r1-distill-llama-8b.md) | `POST /v1/chat/completions` | [docs](https://docs.api.nvidia.com/nim/reference/llm-apis) |
| [Create Chat Completion (deepseek-ai/deepseek-r1-distill-qwen-14b)](actions/create-chat-completion-deepseek-ai-deepseek-r1-distill-qwen-14b.md) | `POST /v1/chat/completions` | [docs](https://docs.api.nvidia.com/nim/reference/llm-apis) |
| [Create Chat Completion (deepseek-ai/deepseek-r1-distill-qwen-32b)](actions/create-chat-completion-deepseek-ai-deepseek-r1-distill-qwen-32b.md) | `POST /v1/chat/completions` | [docs](https://docs.api.nvidia.com/nim/reference/llm-apis) |
| [Create Chat Completion (deepseek-ai/deepseek-r1-distill-qwen-7b)](actions/create-chat-completion-deepseek-ai-deepseek-r1-distill-qwen-7b.md) | `POST /v1/chat/completions` | [docs](https://docs.api.nvidia.com/nim/reference/llm-apis) |
| [Create Chat Completion (deepseek-ai/deepseek-v3.1)](actions/create-chat-completion-deepseek-ai-deepseek-v3-1.md) | `POST /v1/chat/completions` | [docs](https://docs.api.nvidia.com/nim/reference/llm-apis) |
| [Create Chat Completion (deepseek-ai/deepseek-v3.1-terminus)](actions/create-chat-completion-deepseek-ai-deepseek-v3-1-terminus.md) | `POST /v1/chat/completions` | [docs](https://docs.api.nvidia.com/nim/reference/llm-apis) |
| [Create Chat Completion (deepseek-ai/deepseek-v3.2)](actions/create-chat-completion-deepseek-ai-deepseek-v3-2.md) | `POST /v1/chat/completions` | [docs](https://docs.api.nvidia.com/nim/reference/llm-apis) |
| [Create Chat Completion (google/gemma-2-27b-it)](actions/create-chat-completion-google-gemma-2-27b-it.md) | `POST /v1/chat/completions` | [docs](https://docs.api.nvidia.com/nim/reference/llm-apis) |
| [Create Chat Completion (google/gemma-2-2b-it)](actions/create-chat-completion-google-gemma-2-2b-it.md) | `POST /v1/chat/completions` | [docs](https://docs.api.nvidia.com/nim/reference/llm-apis) |
| [Create Chat Completion (google/gemma-2-9b-it)](actions/create-chat-completion-google-gemma-2-9b-it.md) | `POST /v1/chat/completions` | [docs](https://docs.api.nvidia.com/nim/reference/llm-apis) |
| [Create Chat Completion (google/gemma-3-1b-it)](actions/create-chat-completion-google-gemma-3-1b-it.md) | `POST /v1/chat/completions` | [docs](https://docs.api.nvidia.com/nim/reference/llm-apis) |
| [Create Chat Completion (google/gemma-7b)](actions/create-chat-completion-google-gemma-7b.md) | `POST /v1/chat/completions` | [docs](https://docs.api.nvidia.com/nim/reference/llm-apis) |
| [Create Chat Completion (google/shieldgemma-9b)](actions/create-chat-completion-google-shieldgemma-9b.md) | `POST /v1/chat/completions` | [docs](https://docs.api.nvidia.com/nim/reference/llm-apis) |
| [Create Chat Completion (ibm/granite-3_3-8b-instruct)](actions/create-chat-completion-ibm-granite-3-3-8b-instruct.md) | `POST /v1/chat/completions` | [docs](https://docs.api.nvidia.com/nim/reference/llm-apis) |
| [Create Chat Completion (ibm/granite-guardian-3.0-8b)](actions/create-chat-completion-ibm-granite-guardian-3-0-8b.md) | `POST /v1/chat/completions` | [docs](https://docs.api.nvidia.com/nim/reference/llm-apis) |
| [Create Chat Completion (igenius/colosseum_355b_instruct_16k)](actions/create-chat-completion-igenius-colosseum-355b-instruct-16k.md) | `POST /v1/chat/completions` | [docs](https://docs.api.nvidia.com/nim/reference/llm-apis) |
| [Create Chat Completion (institute-of-science-tokyo/llama-3.1-swallow-70b-instruct-v01)](actions/create-chat-completion-institute-of-science-tokyo-llama-3-1-swallow-70b-instruct-v01.md) | `POST /v1/chat/completions` | [docs](https://docs.api.nvidia.com/nim/reference/llm-apis) |
| [Create Chat Completion (marin/marin-8b-instruct)](actions/create-chat-completion-marin-marin-8b-instruct.md) | `POST /v1/chat/completions` | [docs](https://docs.api.nvidia.com/nim/reference/llm-apis) |
| [Create Chat Completion (meta/llama3-8b-instruct)](actions/create-chat-completion-meta-llama3-8b-instruct.md) | `POST /v1/chat/completions` | [docs](https://docs.api.nvidia.com/nim/reference/llm-apis) |
| [Create Chat Completion (microsoft/phi-3-medium-128k-instruct)](actions/create-chat-completion-microsoft-phi-3-medium-128k-instruct.md) | `POST /v1/chat/completions` | [docs](https://docs.api.nvidia.com/nim/reference/llm-apis) |
| [Create Chat Completion (microsoft/phi-3-mini-128k-instruct)](actions/create-chat-completion-microsoft-phi-3-mini-128k-instruct.md) | `POST /v1/chat/completions` | [docs](https://docs.api.nvidia.com/nim/reference/llm-apis) |
| [Create Chat Completion (mistralai/mistral-7b-instruct)](actions/create-chat-completion-mistralai-mistral-7b-instruct.md) | `POST /v1/chat/completions` | [docs](https://docs.api.nvidia.com/nim/reference/llm-apis) |
| [Create Chat Completion (mistralai/mistral-large-2-instruct)](actions/create-chat-completion-mistralai-mistral-large-2-instruct.md) | `POST /v1/chat/completions` | [docs](https://docs.api.nvidia.com/nim/reference/llm-apis) |
| [Create Chat Completion (nvidia/llama3-chatqa-1.5-70b)](actions/create-chat-completion-nvidia-llama3-chatqa-1-5-70b.md) | `POST /v1/chat/completions` | [docs](https://docs.api.nvidia.com/nim/reference/llm-apis) |
| [Create Chat Completion (nvidia/nemotron-4-340b-instruct)](actions/create-chat-completion-nvidia-nemotron-4-340b-instruct.md) | `POST /v1/chat/completions` | [docs](https://docs.api.nvidia.com/nim/reference/llm-apis) |
| [Create Chat Completion (nvidia/nemotron-4-340b-reward)](actions/create-chat-completion-nvidia-nemotron-4-340b-reward.md) | `POST /v1/chat/completions` | [docs](https://docs.api.nvidia.com/nim/reference/llm-apis) |
| [List Models](actions/list-models.md) | `GET /v1/models` | [docs](https://docs.api.nvidia.com/nim/reference/llm-apis) |
