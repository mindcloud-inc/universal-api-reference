# <img src="https://images.mindcloud.co/apps/icons/download-5_1776186918032.png" alt="Hamsa logo" width="28" height="28"> Hamsa: Universal API

Build and manage AI voice agents for phone and web

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/hamsa/latest
- **Category:** Support / Contact Center
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://tryhamsa.com
- **Vendor API docs:** https://docs.tryhamsa.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Project By API Key](actions/get-project-by-api-key.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/get-project-by-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Actions

| Action | Method | Description |
| --- | --- | --- |
| [Create Web Tool](actions/create-web-tool.md) | POST | Creates a new web tool in Hamsa. |
| [Generate Speech to Text Transcription](actions/generate-speech-to-text-transcription.md) | POST | Generates a speech-to-text transcription with Hamsa. |
| [Generate Streamed Text to Speech File Data](actions/generate-streamed-text-to-speech-file-data.md) | POST | Generates streamed text-to-speech audio data with Hamsa. |
| [Generate Text to Speech File Data](actions/generate-text-to-speech-file-data.md) | POST | Generates text-to-speech file data with Hamsa. |
| [Get a web tool by ID](actions/get-web-tool-by-id.md) | GET | Retrieves a web tool from Hamsa. |
| [List Web Tools](actions/list-web-tools.md) | GET | Retrieves available web tools from Hamsa. |

### Conversations

| Action | Method | Description |
| --- | --- | --- |
| [Clone Voice Agent](actions/clone-voice-agent.md) | POST | Clones a voice agent in Hamsa. |
| [Create Voice Agent](actions/create-voice-agent.md) | POST | Creates a new voice agent in Hamsa. |
| [Get Voice Agent By Id](actions/get-voice-agent-by-id.md) | GET | Retrieves a voice agent from Hamsa. |
| [List Voice Agents](actions/list-voice-agents.md) | GET | Retrieves voice agents from your Hamsa project. |
| [Update Voice Agent](actions/update-voice-agent.md) | PUT | Updates an existing voice agent in Hamsa. |

### Jobs

| Action | Method | Description |
| --- | --- | --- |
| [Call Voice Agent via Twilio](actions/call-voice-agent-via-twilio.md) | POST | Starts a Twilio call to a Hamsa voice agent. |
| [Create AI Content](actions/create-ai-content.md) | POST | Creates AI content in Hamsa. |
| [Create Customized AI Content](actions/create-customized-ai-content.md) | POST | Creates customized AI content in Hamsa. |
| [Generate Text to Speech Route](actions/generate-text-to-speech-route.md) | POST | Generates text-to-speech output in Hamsa. |
| [Get AI Content](actions/get-ai-content.md) | GET | Retrieves AI content from Hamsa. |
| [Get AI Content Cost Estimate](actions/get-ai-content-cost-estimate.md) | GET | Retrieves an AI content cost estimate from Hamsa. |

### Keywords

| Action | Method | Description |
| --- | --- | --- |
| [Create Voice Dictionary](actions/create-voice-dictionary.md) | POST | Creates a new voice dictionary in Hamsa. |
| [Update Voice Dictionary](actions/update-voice-dictionary.md) | PUT | Updates an existing voice dictionary in Hamsa. |

### Metrics

| Action | Method | Description |
| --- | --- | --- |
| [Get Overview Analytics](actions/get-overview-analytics.md) | GET | Retrieves voice agent overview analytics from Hamsa. |
| [Get Performance Analytics](actions/get-performance-analytics.md) | GET | Retrieves voice agent performance analytics from Hamsa. |
| [Get Satisfaction and Outcome Analytics](actions/get-satisfaction-and-outcome-analytics.md) | GET | Retrieves voice agent satisfaction and outcome analytics from Hamsa. |
| [Get Usage Statistics Chart](actions/get-usage-statistics-chart.md) | GET | Retrieves usage statistics chart data from Hamsa. |
| [Get Usage Statistics Numbers](actions/get-usage-statistics-numbers.md) | GET | Retrieves usage statistic totals from Hamsa. |

### Phone Numbers

| Action | Method | Description |
| --- | --- | --- |
| [Assign Phone Number to Voice Agent](actions/assign-phone-number-to-voice-agent.md) | POST | Assigns a phone number to a Hamsa voice agent. |
| [Assign Twilio Number to Voice Agent](actions/assign-twilio-number-to-voice-agent.md) | POST | Assigns a Twilio number to a Hamsa voice agent. |
| [Get Phone Number by its ID](actions/get-phone-number-by-its-id.md) | GET | Retrieves a phone number from Hamsa by ID. |
| [List User Phone Numbers](actions/list-user-phone-numbers.md) | GET | Retrieves your phone numbers from Hamsa. |
| [Unassign Phone Number from Voice Agent](actions/unassign-phone-number-from-voice-agent.md) | POST | Unassigns a phone number from a Hamsa voice agent. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Get Project By API Key](actions/get-project-by-api-key.md) | GET | Retrieves a project from Hamsa by API key. |

