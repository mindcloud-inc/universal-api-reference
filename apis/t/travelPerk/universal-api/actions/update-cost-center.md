# TravelPerk: Update Cost Center

Updates an existing cost center in TravelPerk.

```
PUT https://connect.mindcloud.co/v1/universal/travelPerk/latest/actions/update-cost-center
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TravelPerk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/travelPerk/latest/actions/update-cost-center" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "costCenterId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/travelPerk/latest/actions/update-cost-center', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "costCenterId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `costCenterId` | string | yes | The cost center identifier to update. |
| `name` | string | no | Updated name for the cost center. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "approver": {},
      "approver_id": "string",
      "archived": true,
      "count_users": 1,
      "delegate": {},
      "delegate_expiry": "string",
      "delegate_id": "string",
      "id": "string",
      "name": "Ava Chen",
      "users": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `approver` | object |  |
| `approver_id` | string |  |
| `archived` | boolean |  |
| `count_users` | number |  |
| `delegate` | object |  |
| `delegate_expiry` | string |  |
| `delegate_id` | string |  |
| `id` | string |  |
| `name` | string |  |
| `users` | array<object> |  |

## Native endpoint

Through the native TravelPerk API, this operation is `PATCH /cost_centers/:costCenterId` (base URL `https://api.sandbox-travelperk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-cost-center.md) for the provider-specific parameters and requirements.

