# Hamsa: Native API Reference

A consolidated summary of Hamsa's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://docs.tryhamsa.com
- **API base URL:** `https://api.tryhamsa.com`

## Authentication

### API Key

Use a Hamsa API key from the dashboard.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.tryhamsa.com/create-api-keys)

## API conventions

Responses from this API use JSON.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Assign Phone Number to Voice Agent](actions/assign-phone-number-to-voice-agent.md) | `POST /v1/voice-agents/assign-number` | [docs](https://docs.tryhamsa.com/api-reference/endpoint/assign-phone-number) |
| [Assign Twilio Number to Voice Agent](actions/assign-twilio-number-to-voice-agent.md) | `POST /v1/voice-agents/twilio/assign-number` | [docs](https://docs.tryhamsa.com/api-reference/endpoint/assign-twilio-number) |
| [Call Voice Agent via Twilio](actions/call-voice-agent-via-twilio.md) | `POST /v1/voice-agents/twilio/call` | [docs](https://docs.tryhamsa.com/api-reference/endpoint/call-twilio-number) |
| [Clone Voice Agent](actions/clone-voice-agent.md) | `POST /v1/voice-agents/clone` | [docs](https://docs.tryhamsa.com/api-reference/endpoint/clone-voice-agent) |
| [Create AI Content](actions/create-ai-content.md) | `POST /v1/jobs/ai-content` | [docs](https://docs.tryhamsa.com/api-reference/endpoint/create-ai-content) |
| [Create Customized AI Content](actions/create-customized-ai-content.md) | `POST /v1/jobs/ai-content/custom` | [docs](https://docs.tryhamsa.com/api-reference/endpoint/create-customized-ai-content) |
| [Create Voice Agent](actions/create-voice-agent.md) | `POST /v1/voice-agents` | [docs](https://docs.tryhamsa.com/api-reference/endpoint/create-voice-agent) |
| [Create Voice Dictionary](actions/create-voice-dictionary.md) | `POST /v1/voice-agents/voice-dictionaries` | [docs](https://docs.tryhamsa.com/api-reference/endpoint/create-voice-dictionary) |
| [Create Web Tool](actions/create-web-tool.md) | `POST /v2/voice-agents/web-tool` | [docs](https://docs.tryhamsa.com/api-reference/endpoint/v2/create-web-tool) |
| [Generate Speech to Text Transcription](actions/generate-speech-to-text-transcription.md) | `POST /v1/realtime/stt` | [docs](https://docs.tryhamsa.com/api-reference/endpoint/generate-speech-to-text-transcription) |
| [Generate Streamed Text to Speech File Data](actions/generate-streamed-text-to-speech-file-data.md) | `POST /v1/realtime/tts-stream` | [docs](https://docs.tryhamsa.com/api-reference/endpoint/generate-streamed-text-to-speech-file-data) |
| [Generate Text to Speech File Data](actions/generate-text-to-speech-file-data.md) | `POST /v1/realtime/tts` | [docs](https://docs.tryhamsa.com/api-reference/endpoint/generate-text-to-speech-file-data) |
| [Generate Text to Speech Route](actions/generate-text-to-speech-route.md) | `POST /v1/jobs/text-to-speech` | [docs](https://docs.tryhamsa.com/api-reference/endpoint/generate-text-to-speech) |
| [Get AI Content](actions/get-ai-content.md) | `GET /v1/jobs/ai-content` | [docs](https://docs.tryhamsa.com/api-reference/endpoint/get-ai-content) |
| [Get AI Content Cost Estimate](actions/get-ai-content-cost-estimate.md) | `GET /v1/jobs/ai-content/estimate` | [docs](https://docs.tryhamsa.com/api-reference/endpoint/get-ai-content-cost-estimate) |
| [Get Overview Analytics](actions/get-overview-analytics.md) | `GET /v1/agent-analytics/overview` | [docs](https://docs.tryhamsa.com/api-reference/endpoint/get-overview-analytics) |
| [Get Performance Analytics](actions/get-performance-analytics.md) | `GET /v1/agent-analytics/performance` | [docs](https://docs.tryhamsa.com/api-reference/endpoint/get-performance-analytics) |
| [Get Phone Number by its ID](actions/get-phone-number-by-its-id.md) | `GET /v1/voice-agents/phone-number` | [docs](https://docs.tryhamsa.com/api-reference/endpoint/get-phone-number) |
| [Get Project By API Key](actions/get-project-by-api-key.md) | `GET /v1/projects/by-api-key` | [docs](https://docs.tryhamsa.com/api-reference/endpoint/get-project-by-api-key) |
| [Get Satisfaction and Outcome Analytics](actions/get-satisfaction-and-outcome-analytics.md) | `GET /v1/agent-analytics/satisfaction` | [docs](https://docs.tryhamsa.com/api-reference/endpoint/get-satisfaction-analytics) |
| [Get Usage Statistics Chart](actions/get-usage-statistics-chart.md) | `GET /v1/projects/statistics/chart` | [docs](https://docs.tryhamsa.com/api-reference/endpoint/statistics-chart) |
| [Get Usage Statistics Numbers](actions/get-usage-statistics-numbers.md) | `GET /v1/projects/statistics/numbers` | [docs](https://docs.tryhamsa.com/api-reference/endpoint/statistics-numbers) |
| [Get Voice Agent By Id](actions/get-voice-agent-by-id.md) | `GET /v1/voice-agents/:voiceAgentId` | [docs](https://docs.tryhamsa.com/api-reference/endpoint/get-voice-agent-by-id) |
| [Get a web tool by ID](actions/get-web-tool-by-id.md) | `GET /v1/voice-agents/web-tool/{id}` | [docs](https://docs.tryhamsa.com/api-reference/get-a-web-tool-by-id) |
| [List User Phone Numbers](actions/list-user-phone-numbers.md) | `GET /v1/voice-agents/phone-number/list` | [docs](https://docs.tryhamsa.com/api-reference/endpoint/list-phone-numbers) |
| [List Voice Agents](actions/list-voice-agents.md) | `GET /v2/voice-agents` | [docs](https://docs.tryhamsa.com/api-reference/endpoint/list-voice-agents-v2) |
| [List Web Tools](actions/list-web-tools.md) | `GET /v2/voice-agents/web-tool/list` | [docs](https://docs.tryhamsa.com/api-reference/endpoint/v2/list-web-tools) |
| [Unassign Phone Number from Voice Agent](actions/unassign-phone-number-from-voice-agent.md) | `POST /v1/voice-agents/unassign` | [docs](https://docs.tryhamsa.com/api-reference/endpoint/unassign-phone-number) |
| [Update Voice Agent](actions/update-voice-agent.md) | `PATCH /v2/voice-agents/:voiceAgentId` | [docs](https://docs.tryhamsa.com/api-reference/endpoint/update-voice-agent-v2) |
| [Update Voice Dictionary](actions/update-voice-dictionary.md) | `PATCH /v1/voice-agents/voice-dictionaries/:voiceDictionaryId` | [docs](https://docs.tryhamsa.com/api-reference/endpoint/update-voice-dictionary) |
