# Teamgate: Update Deal

Updates a deal in Teamgate.

```
PUT https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/update-deal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teamgate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/update-deal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "dealId": "79"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/update-deal', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "dealId": "79"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dealId` | string | yes | Deal ID to update. Example: `79`. |
| `name` | string | no | Updated deal name. Example: `Codex Stage 3 Deal Updated`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cost": {},
      "created": {},
      "estimatedClosureDate": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "isDeleted": "string",
      "name": "Ava Chen",
      "owner": {},
      "pipeline": {},
      "price": {},
      "source": {},
      "stage": {},
      "starred": "string",
      "status": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cost` | object |  |
| `created` | object |  |
| `estimatedClosureDate` | date |  |
| `id` | number |  |
| `isDeleted` | string |  |
| `name` | string |  |
| `owner` | object |  |
| `pipeline` | object |  |
| `price` | object |  |
| `source` | object |  |
| `stage` | object |  |
| `starred` | string |  |
| `status` | object |  |

## Native endpoint

Through the native Teamgate API, this operation is `PUT /deals/:deal_id` (base URL `https://api.teamgate.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-deal.md) for the provider-specific parameters and requirements.

