# <img src="https://images.mindcloud.co/apps/icons/1722190046010-bd1a05f5a5309646_1773693562653.png" alt="Vapi logo" width="28" height="28"> Vapi: Universal API

Manage Vapi assistants, calls, chats, tools, files, sessions, squads, and campaigns with the Vapi management API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/vapi/latest
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://vapi.ai
- **Vendor API docs:** https://docs.vapi.ai/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Assistants](actions/list-assistants.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vapi/latest/actions/list-assistants?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Assistant

| Action | Method | Description |
| --- | --- | --- |
| [Create Assistant](actions/create-assistant.md) | POST | Creates a new assistant in Vapi. |
| [Delete Assistant](actions/delete-assistant.md) | DELETE | Deletes an existing assistant from Vapi. |
| [Get Assistant](actions/get-assistant.md) | GET | Retrieves an assistant from Vapi by ID. |
| [List Assistants](actions/list-assistants.md) | GET | Retrieves a list of assistants from Vapi. |
| [Update Assistant](actions/update-assistant.md) | PUT | Updates an existing assistant in Vapi. |

### Call

| Action | Method | Description |
| --- | --- | --- |
| [Create Call](actions/create-call.md) | POST | Creates a new call in Vapi. |
| [Delete Call](actions/delete-call.md) | DELETE | Deletes an existing call from Vapi. |
| [Get Call](actions/get-call.md) | GET | Retrieves a call from Vapi by ID. |
| [List Calls](actions/list-calls.md) | GET | Retrieves a list of calls from Vapi. |
| [Update Call](actions/update-call.md) | PUT | Updates an existing call in Vapi. |

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Create Campaign](actions/create-campaign.md) | POST | Creates a new campaign in Vapi. |
| [Delete Campaign](actions/delete-campaign.md) | DELETE | Deletes an existing campaign from Vapi. |
| [Get Campaign](actions/get-campaign.md) | GET | Retrieves a campaign from Vapi by ID. |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves a list of campaigns from Vapi. |
| [Update Campaign](actions/update-campaign.md) | PUT | Updates an existing campaign in Vapi. |

### Chat

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat](actions/create-chat.md) | POST | Creates a new chat in Vapi. |
| [Delete Chat](actions/delete-chat.md) | DELETE | Deletes an existing chat from Vapi. |
| [Get Chat](actions/get-chat.md) | GET | Retrieves a chat from Vapi by ID. |
| [List Chats](actions/list-chats.md) | GET | Retrieves a list of chats from Vapi. |

### Chat Response

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat Response](actions/create-chat-response.md) | POST | Creates an OpenAI-compatible chat response in Vapi. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Delete File](actions/delete-file.md) | DELETE | Deletes an existing file from Vapi. |
| [Get File](actions/get-file.md) | GET | Retrieves a file from Vapi by ID. |
| [List Files](actions/list-files.md) | GET | Retrieves a list of files from Vapi. |
| [Update File](actions/update-file.md) | PUT | Updates an existing file in Vapi. |
| [Upload File](actions/upload-file.md) | POST | Uploads a file to the Vapi knowledge base. |

### Session

| Action | Method | Description |
| --- | --- | --- |
| [Create Session](actions/create-session.md) | POST | Creates a new session in Vapi. |
| [Delete Session](actions/delete-session.md) | DELETE | Deletes an existing session from Vapi. |
| [Get Session](actions/get-session.md) | GET | Retrieves a session from Vapi by ID. |
| [List Sessions](actions/list-sessions.md) | GET | Retrieves a list of sessions from Vapi. |
| [Update Session](actions/update-session.md) | PUT | Updates an existing session in Vapi. |

### Squad

| Action | Method | Description |
| --- | --- | --- |
| [Create Squad](actions/create-squad.md) | POST | Creates a new squad in Vapi. |
| [Delete Squad](actions/delete-squad.md) | DELETE | Deletes an existing squad from Vapi. |
| [Get Squad](actions/get-squad.md) | GET | Retrieves a squad from Vapi by ID. |
| [List Squads](actions/list-squads.md) | GET | Retrieves a list of squads from Vapi. |
| [Update Squad](actions/update-squad.md) | PUT | Updates an existing squad in Vapi. |

### Tool

| Action | Method | Description |
| --- | --- | --- |
| [Create Tool](actions/create-tool.md) | POST | Creates a new tool in Vapi. |
| [Delete Tool](actions/delete-tool.md) | DELETE | Deletes an existing tool from Vapi. |
| [Get Tool](actions/get-tool.md) | GET | Retrieves a tool from Vapi by ID. |
| [List Tools](actions/list-tools.md) | GET | Retrieves a list of tools from Vapi. |
| [Update Tool](actions/update-tool.md) | PUT | Updates an existing tool in Vapi. |

