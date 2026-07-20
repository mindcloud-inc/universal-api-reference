# <img src="https://images.mindcloud.co/apps/icons/images-19_1774903577688.jpeg" alt="Fluents logo" width="28" height="28"> Fluents: Universal API

Build and manage Fluents voice AI resources including agents, calls, phone numbers, prompts, voices, actions, webhooks, and account connections. Validated against a Fluents tenant with a UI-created API key connection.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/fluents/latest
- **Category:** Support / Contact Center
- **Actions:** 42
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.fluents.ai
- **Vendor API docs:** https://docs.fluents.ai/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Agents](actions/list-agents.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fluents/latest/actions/list-agents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (42)

### Actions

| Action | Method | Description |
| --- | --- | --- |
| [Create Action](actions/create-action.md) | POST | Creates a new action in Fluents. |
| [Delete Action](actions/delete-action.md) | DELETE | Deletes an existing action from Fluents. |
| [Get Action](actions/get-action.md) | GET | Retrieves an action from your Fluents account. |
| [List Actions](actions/list-actions.md) | GET | Retrieves actions from your Fluents account. |
| [Update Action](actions/update-action.md) | PUT | Updates an existing action in Fluents. |

### Calls

| Action | Method | Description |
| --- | --- | --- |
| [Create Call](actions/create-call.md) | POST | Creates a new call in Fluents. |
| [End Call](actions/end-call.md) | PUT | Ends an active call in Fluents. |
| [Get Call](actions/get-call.md) | GET | Retrieves a call from your Fluents account. |
| [List Calls](actions/list-calls.md) | GET | Retrieves calls from your Fluents account. |

### Connections

| Action | Method | Description |
| --- | --- | --- |
| [Create Account Connection](actions/create-account-connection.md) | POST | Creates a new account connection in Fluents. |
| [Get Account Connection](actions/get-account-connection.md) | GET | Retrieves an account connection from Fluents. |
| [List Account Connections](actions/list-account-connections.md) | GET | Retrieves account connections from your Fluents account. |
| [Update Account Connection](actions/update-account-connection.md) | PUT | Updates an existing account connection in Fluents. |

### Phone Numbers

| Action | Method | Description |
| --- | --- | --- |
| [Buy Number](actions/buy-number.md) | POST | Creates a new phone number purchase in Fluents. |
| [Cancel Number](actions/cancel-number.md) | DELETE | Cancels an existing phone number from Fluents. |
| [Detach Number](actions/detach-number.md) | PUT | Detaches a phone number in Fluents. |
| [Get Number](actions/get-number.md) | GET | Retrieves a phone number from Fluents. |
| [Link Number](actions/link-number.md) | PUT | Links a phone number in Fluents. |
| [List Available Numbers](actions/list-available-numbers.md) | GET | Retrieves available phone numbers from Fluents. |
| [List Numbers](actions/list-numbers.md) | GET | Retrieves phone numbers from your Fluents account. |
| [Update Number](actions/update-number.md) | PUT | Updates an existing phone number in Fluents. |

### Recordings

| Action | Method | Description |
| --- | --- | --- |
| [Get Recording](actions/get-recording.md) | GET | Retrieves a call recording from Fluents. |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [Create Prompt](actions/create-prompt.md) | POST | Creates a new prompt in Fluents. |
| [Delete Prompt](actions/delete-prompt.md) | DELETE | Deletes an existing prompt from Fluents. |
| [Get Prompt](actions/get-prompt.md) | GET | Retrieves a prompt from your Fluents account. |
| [List Prompts](actions/list-prompts.md) | GET | Retrieves prompts from your Fluents account. |
| [Update Prompt](actions/update-prompt.md) | PUT | Updates an existing prompt in Fluents. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Create Agent](actions/create-agent.md) | POST | Creates a new agent in Fluents. |
| [Create Voice](actions/create-voice.md) | POST | Creates a new voice in Fluents. |
| [Delete Agent](actions/delete-agent.md) | DELETE | Deletes an existing agent from Fluents. |
| [Delete Voice](actions/delete-voice.md) | DELETE | Deletes an existing voice from Fluents. |
| [Get Agent](actions/get-agent.md) | GET | Retrieves an agent from your Fluents account. |
| [Get Voice](actions/get-voice.md) | GET | Retrieves a voice from your Fluents account. |
| [List Agents](actions/list-agents.md) | GET | Retrieves agents from your Fluents account. |
| [List Voices](actions/list-voices.md) | GET | Retrieves voices from your Fluents account. |
| [Update Agent](actions/update-agent.md) | PUT | Updates an existing agent in Fluents. |
| [Update Voice](actions/update-voice.md) | PUT | Updates an existing voice in Fluents. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Fluents. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from Fluents. |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves a webhook from your Fluents account. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from your Fluents account. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook in Fluents. |

