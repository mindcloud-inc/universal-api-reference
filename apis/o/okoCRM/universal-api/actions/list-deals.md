# OkoCRM: List deals

Retrieves deals from OkoCRM.

```
GET https://connect.mindcloud.co/v1/universal/okoCRM/latest/actions/list-deals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OkoCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/okoCRM/latest/actions/list-deals?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/okoCRM/latest/actions/list-deals?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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
| `updated_at` | date |  |
| `url` | string |  |
| `user_id` | number |  |

## Native endpoint

Through the native OkoCRM API, this operation is `GET /leads/` (base URL `https://api.okocrm.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-deals.md) for the provider-specific parameters and requirements.

