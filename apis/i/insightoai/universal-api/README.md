# <img src="https://images.mindcloud.co/apps/icons/insightoai_1774878875436.png" alt="Insighto.ai logo" width="28" height="28"> Insighto.ai: Universal API

Build, manage, and operate AI phone-call and chat agents, assistants, widgets, data sources, intents, contacts, and conversations in Insighto.ai.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/insightoai/latest
- **Category:** Support / Contact Center
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://insighto.ai/
- **Vendor API docs:** https://docs.insighto.ai/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Assistants](actions/list-assistants.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/list-assistants?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Assistant

| Action | Method | Description |
| --- | --- | --- |
| [Add Datasource To Assistant](actions/add-datasource-to-assistant.md) | PUT |  |
| [Add Intent To Assistant](actions/add-intent-to-assistant.md) | PUT |  |
| [Create Assistant](actions/create-assistant.md) | POST |  |
| [Delete Assistant By Id](actions/delete-assistant-by-id.md) | DELETE |  |
| [Get Assistant By Id](actions/get-assistant-by-id.md) | GET |  |
| [List Assistants](actions/list-assistants.md) | GET |  |
| [Update Assistant By Id](actions/update-assistant-by-id.md) | PUT |  |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Get Contact By Id](actions/get-contact-by-id.md) | GET |  |
| [List Contacts](actions/list-contacts.md) | GET |  |
| [Update Contact By Id](actions/update-contact-by-id.md) | PUT |  |
| [Upsert Contact By Email Or Phone Number](actions/upsert-contact-by-email-or-phone-number.md) | POST |  |

### Conversation

| Action | Method | Description |
| --- | --- | --- |
| [Get Conversation By Id](actions/get-conversation-by-id.md) | GET |  |
| [Get Transcript Of A Conversation](actions/get-conversation-transcript.md) | GET |  |
| [List Conversations](actions/list-conversations.md) | GET |  |
| [Get List Of Conversations By Contact Id](actions/list-conversations-by-contact-id.md) | GET |  |

### Data Source

| Action | Method | Description |
| --- | --- | --- |
| [Add Datasourcefile](actions/add-datasource-file.md) | PUT |  |
| [Add Datasourcefile Text Blob](actions/add-datasource-text-blob.md) | PUT |  |
| [Create Data Source](actions/create-data-source.md) | POST |  |
| [Delete Datasource By Id](actions/delete-datasource-by-id.md) | DELETE |  |
| [Get Datasource By Id](actions/get-datasource-by-id.md) | GET |  |
| [List Data Sources](actions/list-data-sources.md) | GET |  |

### Data Source File

| Action | Method | Description |
| --- | --- | --- |
| [List Data Source Files For Data Source Id](actions/list-data-source-files-by-datasource-id.md) | GET |  |

### Intent

| Action | Method | Description |
| --- | --- | --- |
| [Create Intent](actions/create-intent.md) | POST |  |
| [Get Intent By Id](actions/get-intent-by-id.md) | GET |  |
| [List Intents](actions/list-intents.md) | GET |  |

### Widget

| Action | Method | Description |
| --- | --- | --- |
| [Create Widget](actions/create-widget.md) | POST |  |
| [Delete Widget By Id](actions/delete-widget-by-id.md) | DELETE |  |
| [Get Widget By Id](actions/get-widget-by-id.md) | GET |  |
| [List Widgets](actions/list-widgets.md) | GET |  |
| [Update Widget By Id](actions/update-widget-by-id.md) | PUT |  |

