# <img src="https://images.mindcloud.co/apps/icons/favicon-18_1775593462102.png" alt="DIDWW SMS OUT logo" width="28" height="28"> DIDWW SMS OUT: Universal API

Send outbound SMS messages through a DIDWW HTTP OUT trunk and verify HTTP OUT credentials without delivering a real message.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dIDWWSMSOUT/latest
- **Category:** Marketing
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.didww.com/
- **Vendor API docs:** https://doc.didww.com/sms/sms-trunks/technical-data/http-specification.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Send Bulk SMS With Campaign](actions/send-bulk-sms-with-campaign.md):

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dIDWWSMSOUT/latest/actions/send-bulk-sms-with-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "destinations": "string",
  "content": "string",
  "campaignId": "string"
}'
```

## Actions (4)

### Bulk Outbound Message

| Action | Method | Description |
| --- | --- | --- |
| [Send Bulk SMS With Campaign](actions/send-bulk-sms-with-campaign.md) | POST | Creates bulk outbound SMS messages in DIDWW SMS OUT with a campaign ID. |
| [Send Bulk SMS With Source](actions/send-bulk-sms-with-source.md) | POST | Creates bulk outbound SMS messages in DIDWW SMS OUT with a source DID. |

### Outbound Message

| Action | Method | Description |
| --- | --- | --- |
| [Send SMS With Campaign](actions/send-sms-with-campaign.md) | POST | Creates an outbound SMS in DIDWW SMS OUT with a campaign ID. |
| [Send SMS With Source](actions/send-sms-with-source.md) | POST | Creates an outbound SMS in DIDWW SMS OUT with a source DID. |

