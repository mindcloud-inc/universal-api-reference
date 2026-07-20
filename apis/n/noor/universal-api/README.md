# <img src="https://images.mindcloud.co/apps/icons/app-icon3x_1775668552097.png" alt="Noor logo" width="28" height="28"> Noor: Universal API

Chat, collaborate, and share updates with your team

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/noor/latest
- **Category:** Communication / Team Messaging
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://noor.to
- **Vendor API docs:** https://usenoor.notion.site/Noor-Docs-48ff40fb312547a0aedfd5c0450d7a59

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Space Members](actions/list-space-members.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/noor/latest/actions/list-space-members?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Send Message](actions/send-message.md) | POST | Creates a message in a Noor thread. |

### Space Member

| Action | Method | Description |
| --- | --- | --- |
| [List Space Members](actions/list-space-members.md) | GET | Retrieves members for a Noor space. |

