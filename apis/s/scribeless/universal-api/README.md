# <img src="https://images.mindcloud.co/apps/icons/scribeless_1775671113250.png" alt="Scribeless logo" width="28" height="28"> Scribeless: Universal API

Send handwritten mailers with Scribeless by creating recipients for Scribeless campaigns.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/scribeless/latest
- **Category:** Marketing
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://scribeless.co/
- **Vendor API docs:** https://docs.scribeless.co/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Create Recipient](actions/create-recipient.md):

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/scribeless/latest/actions/create-recipient" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": "string",
  "data": {}
}'
```

## Actions (2)

### Recipient

| Action | Method | Description |
| --- | --- | --- |
| [Create Recipient](actions/create-recipient.md) | POST |  |
| [Create Recipients](actions/create-recipients.md) | POST |  |

