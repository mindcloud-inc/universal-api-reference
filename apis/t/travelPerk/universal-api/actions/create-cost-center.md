# TravelPerk: Create Cost Center

Creates a new cost center in TravelPerk.

```
POST https://connect.mindcloud.co/v1/universal/travelPerk/latest/actions/create-cost-center
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TravelPerk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/travelPerk/latest/actions/create-cost-center" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/travelPerk/latest/actions/create-cost-center', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name of the cost center to create. |

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

Through the native TravelPerk API, this operation is `POST /cost_centers` (base URL `https://api.sandbox-travelperk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-cost-center.md) for the provider-specific parameters and requirements.

