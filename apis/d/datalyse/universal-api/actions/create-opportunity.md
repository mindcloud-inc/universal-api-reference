# Datalyse: Create Opportunity

Creates a new opportunity in Datalyse.

```
POST https://connect.mindcloud.co/v1/universal/datalyse/latest/actions/create-opportunity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datalyse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/datalyse/latest/actions/create-opportunity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "amount": "string",
  "currency": "string",
  "description": "string",
  "leadId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/datalyse/latest/actions/create-opportunity', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "amount": "string",
    "currency": "string",
    "description": "string",
    "leadId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `agentId` | string | no | Agent ID (optional) Default: `unassigned`. |
| `amount` | string | yes | Total amount |
| `calendarId` | string | no | Calendar task ID (optional) |
| `currency` | string | yes | Currency |
| `description` | string | yes | Description of the opportunity |
| `expectedDate` | string | no | Expected closing date (optional) |
| `leadId` | string | yes | ID of the contact or company |
| `pipeline` | string | no | Pipeline ID (optional) |
| `stageId` | string | no | Stage (optional) |
| `status` | string | no | Status ID Default: `0`. |
| `time` | string | no | Time (optional) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string | API response status |

## Native endpoint

Through the native Datalyse API, this operation is `POST /api/1.0/opportunities/create.json` (base URL `https://api.datalyse.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-opportunity.md) for the provider-specific parameters and requirements.

