# <img src="https://images.mindcloud.co/apps/icons/leverly_1775847283893.png" alt="Leverly logo" width="28" height="28"> Leverly: Universal API

Send leads to Leverly and stop queued calls

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/leverly/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://leverly.com
- **Vendor API docs:** https://leverly.com/kb-categories/integration-instructions/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Create Call](actions/create-call.md):

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/leverly/latest/actions/create-call" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "firstName": "Ava",
  "phone1": "string"
}'
```

## Actions (3)

### Call

| Action | Method | Description |
| --- | --- | --- |
| [Salesforce Stop Call](actions/salesforce-stop-call.md) | DELETE |  |
| [Stop Call](actions/stop-call.md) | DELETE |  |

### Lead

| Action | Method | Description |
| --- | --- | --- |
| [Create Call](actions/create-call.md) | POST |  |

