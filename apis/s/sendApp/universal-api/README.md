# <img src="https://images.mindcloud.co/apps/icons/send-app_1774462906304.png" alt="SendApp logo" width="28" height="28"> SendApp: Universal API

Send WhatsApp text, media, template, and template-list operations through the SendApp Official API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sendApp/latest
- **Category:** Communication / Team Messaging
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://official.sendapp.cloud
- **Vendor API docs:** https://official.sendapp.cloud/apiv3/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Templates](actions/list-templates.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendApp/latest/actions/list-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Send Media Message](actions/send-media-message.md) | POST |  |
| [Send Template Message](actions/send-template-message.md) | POST |  |
| [Send Text Message](actions/send-text-message.md) | POST |  |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [List Templates](actions/list-templates.md) | GET |  |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Health Check](actions/health-check.md) | GET |  |

