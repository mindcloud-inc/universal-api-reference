# TravelPerk: Get Cost Center

Retrieves a cost center from TravelPerk.

```
GET https://connect.mindcloud.co/v1/universal/travelPerk/latest/actions/get-cost-center
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TravelPerk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/travelPerk/latest/actions/get-cost-center?connectionId=$CONNECTION_ID&costCenterId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "costCenterId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/travelPerk/latest/actions/get-cost-center?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `costCenterId` | string | yes | The cost center identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "all_companies": true,
      "approver": {},
      "approver_id": "string",
      "archived": true,
      "companies": [
        {}
      ],
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
| `all_companies` | boolean |  |
| `approver` | object |  |
| `approver_id` | string |  |
| `archived` | boolean |  |
| `companies` | array<object> |  |
| `count_users` | number |  |
| `delegate` | object |  |
| `delegate_expiry` | string |  |
| `delegate_id` | string |  |
| `id` | string |  |
| `name` | string |  |
| `users` | array<object> |  |

## Native endpoint

Through the native TravelPerk API, this operation is `GET /cost_centers/:costCenterId` (base URL `https://api.sandbox-travelperk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-cost-center.md) for the provider-specific parameters and requirements.

