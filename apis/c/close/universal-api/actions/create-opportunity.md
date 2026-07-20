# Close: Create Opportunity

Creates a new opportunity in Close.

```
POST https://connect.mindcloud.co/v1/universal/close/latest/actions/create-opportunity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Close `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/close/latest/actions/create-opportunity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "leadId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/close/latest/actions/create-opportunity', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "leadId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `leadId` | string | yes | Lead ID for this opportunity. |
| `note` | string | no | Opportunity description note. |
| `statusId` | string | no | Opportunity status ID. |
| `value` | number | no | Opportunity value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Created opportunity ID. |

## Native endpoint

Through the native Close API, this operation is `POST /opportunity/` (base URL `https://api.close.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-opportunity.md) for the provider-specific parameters and requirements.

