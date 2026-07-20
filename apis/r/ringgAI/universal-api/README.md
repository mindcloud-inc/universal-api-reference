# <img src="https://images.mindcloud.co/apps/icons/ringg-ai_1774021990073.png" alt="Ringg AI logo" width="28" height="28"> Ringg AI: Universal API

Manage Ringg AI assistants, calls, campaigns, and analytics

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/ringgAI/latest
- **Category:** Support / Contact Center
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.ringg.ai
- **Vendor API docs:** https://docs.ringg.ai/api-reference/quick-start/guide

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Workspace Info](actions/get-workspace-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/get-workspace-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Api Key

| Action | Method | Description |
| --- | --- | --- |
| [Regenerate API Key](actions/regenerate-api-key.md) | PUT | Regenerates the API key for a Ringg AI workspace. |

### Assistant

| Action | Method | Description |
| --- | --- | --- |
| [Create Agent](actions/create-agent.md) | POST | Creates an agent in Ringg AI. |
| [Delete Assistant](actions/delete-assistant.md) | DELETE | Archives an assistant in Ringg AI. |
| [Edit Assistant](actions/edit-assistant.md) | PUT | Updates an existing assistant in Ringg AI. |
| [Get Assistant By ID](actions/get-assistant-by-id.md) | GET | Retrieves an assistant from Ringg AI by ID. |
| [Get Assistants](actions/get-assistants.md) | GET | Retrieves assistants from Ringg AI. |
| [Update Agent](actions/update-agent.md) | PUT | Updates an existing agent in Ringg AI. |

### Assistant Voice

| Action | Method | Description |
| --- | --- | --- |
| [Get Assistant Voices](actions/get-assistant-voices.md) | GET | Retrieves assistant voices from Ringg AI. |

### Call

| Action | Method | Description |
| --- | --- | --- |
| [Get Call Details](actions/get-call-details.md) | GET | Retrieves call details from Ringg AI. |
| [Get Call History](actions/get-call-history.md) | GET | Retrieves call history from Ringg AI. |
| [Initiate Individual Call](actions/initiate-individual-call.md) | POST | Initiates an individual outbound call in Ringg AI. |

### Call Export

| Action | Method | Description |
| --- | --- | --- |
| [Download Call History](actions/download-call-history.md) | GET | Downloads call history from Ringg AI as CSV. |

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Get All Campaigns](actions/get-all-campaigns.md) | GET | Retrieves campaigns from Ringg AI. |
| [Start Campaign](actions/start-campaign.md) | POST | Starts a campaign in Ringg AI. |
| [Terminate Calls by Call IDs](actions/terminate-calls-by-call-ids.md) | PUT | Terminates active Ringg AI calls by call IDs. |

### Campaign Analytics

| Action | Method | Description |
| --- | --- | --- |
| [Get Drill-Down Analytics](actions/get-drill-down-analytics.md) | GET | Retrieves drill-down analytics from Ringg AI. |

### Campaign Contact List

| Action | Method | Description |
| --- | --- | --- |
| [Upload Campaign Contact List](actions/upload-campaign-contact-list.md) | POST | Uploads a campaign contact list to Ringg AI. |

### Classification Analytics

| Action | Method | Description |
| --- | --- | --- |
| [Get Classification Analytics](actions/get-classification-analytics.md) | GET | Retrieves classification analytics from Ringg AI. |

### Contact List

| Action | Method | Description |
| --- | --- | --- |
| [Delete Contact List](actions/delete-contact-list.md) | DELETE | Deletes a contact list from Ringg AI. |

### Duration Analytics

| Action | Method | Description |
| --- | --- | --- |
| [Get Duration Distribution](actions/get-duration-distribution.md) | GET | Retrieves duration distribution analytics from Ringg AI. |

### Knowledge Base

| Action | Method | Description |
| --- | --- | --- |
| [Create Knowledge Base](actions/create-knowledge-base.md) | POST | Creates a knowledge base in Ringg AI. |
| [Delete Knowledge Base](actions/delete-knowledge-base.md) | DELETE | Deletes a knowledge base from Ringg AI. |
| [Edit Knowledge Base](actions/edit-knowledge-base.md) | PUT | Updates an existing knowledge base in Ringg AI. |
| [Get All Knowledge Bases](actions/get-all-knowledge-bases.md) | GET | Retrieves knowledge bases from Ringg AI. |
| [Get Knowledge Base by ID](actions/get-knowledge-base-by-id.md) | GET | Retrieves a knowledge base from Ringg AI by ID. |

### Number Analytics

| Action | Method | Description |
| --- | --- | --- |
| [Get Number Analytics](actions/get-number-analytics.md) | GET | Retrieves number analytics from Ringg AI. |

### Platform Analytics

| Action | Method | Description |
| --- | --- | --- |
| [Get Platform Analytics](actions/get-platform-analytics.md) | GET | Retrieves platform analytics from Ringg AI. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Get All User Workspaces](actions/get-all-user-workspaces.md) | GET | Retrieves user workspaces from Ringg AI. |
| [Get Workspace Info](actions/get-workspace-info.md) | GET | Retrieves workspace information from Ringg AI. |

### Workspace Number

| Action | Method | Description |
| --- | --- | --- |
| [Get Workspace Numbers](actions/get-workspace-numbers.md) | GET | Retrieves workspace numbers from Ringg AI. |

### Workspace User

| Action | Method | Description |
| --- | --- | --- |
| [List Workspace Users](actions/list-workspace-users.md) | GET | Retrieves workspace users from Ringg AI. |

