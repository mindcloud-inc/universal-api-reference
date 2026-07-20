# OkoCRM: Get deal

Retrieves deal details from OkoCRM.

```
GET https://connect.mindcloud.co/v1/universal/okoCRM/latest/actions/get-deal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OkoCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/okoCRM/latest/actions/get-deal?connectionId=$CONNECTION_ID&lead_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "lead_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/okoCRM/latest/actions/get-deal?${params}`, {
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
| `lead_id` | number | yes | The OkoCRM deal ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "budget": "string",
      "companies": [
        {}
      ],
      "contacts": [
        {}
      ],
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "name": "Ava Chen",
      "pipeline_id": 1,
      "stages_id": 1,
      "tabs": [
        {}
      ],
      "updated_at": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `budget` | string |  |
| `companies` | array<object> |  |
| `contacts` | array<object> |  |
| `created_at` | date |  |
| `id` | number |  |
| `name` | string |  |
| `pipeline_id` | number |  |
| `stages_id` | number |  |
| `tabs` | array<object> |  |
| `updated_at` | date |  |
| `url` | string |  |
| `user_id` | number |  |

## Native endpoint

Through the native OkoCRM API, this operation is `GET /leads/[:lead_id]/` (base URL `https://api.okocrm.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-deal.md) for the provider-specific parameters and requirements.

