# <img src="https://images.mindcloud.co/apps/icons/pingueen_1774905035157.png" alt="Pingueen logo" width="28" height="28"> Pingueen: Universal API

Manage WhatsApp clients, messages, and templates

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pingueen/latest
- **Category:** Support / Contact Center
- **Actions:** 15
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://pingup.ai
- **Vendor API docs:** https://etinet.gitbook.io/pingueen/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Clients](actions/list-clients.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pingueen/latest/actions/list-clients?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (15)

### Client

| Action | Method | Description |
| --- | --- | --- |
| [Assign Client Agents](actions/assign-client-agents.md) | PUT |  |
| [Create Client](actions/create-client.md) | POST |  |
| [Delete Client](actions/delete-client.md) | DELETE |  |
| [List Clients](actions/list-clients.md) | GET |  |
| [Update Client](actions/update-client.md) | PUT |  |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Send Interactive Message](actions/send-interactive-message.md) | POST |  |
| [Send Interactive Template](actions/send-interactive-template.md) | POST |  |
| [Send Media Message](actions/send-media-message.md) | POST |  |
| [Send Media Template](actions/send-media-template.md) | POST |  |
| [Send Text Message](actions/send-text-message.md) | POST |  |
| [Send Text Template](actions/send-text-template.md) | POST |  |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Create Template](actions/create-template.md) | POST |  |
| [Delete Template](actions/delete-template.md) | DELETE |  |
| [List Templates](actions/list-templates.md) | GET |  |

### User Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get User Info](actions/get-user-info.md) | GET |  |

