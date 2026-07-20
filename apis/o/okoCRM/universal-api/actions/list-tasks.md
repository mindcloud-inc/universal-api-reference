# OkoCRM: List tasks

Retrieves tasks from OkoCRM.

```
GET https://connect.mindcloud.co/v1/universal/okoCRM/latest/actions/list-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OkoCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/okoCRM/latest/actions/list-tasks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/okoCRM/latest/actions/list-tasks?${params}`, {
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
      "company_id": 1,
      "contact_id": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "executor_id": 1,
      "id": 1,
      "lead_id": 1,
      "text": "string",
      "type_id": 1,
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company_id` | number |  |
| `contact_id` | number |  |
| `created_at` | date |  |
| `executor_id` | number |  |
| `id` | number |  |
| `lead_id` | number |  |
| `text` | string |  |
| `type_id` | number |  |
| `updated_at` | date |  |

## Native endpoint

Through the native OkoCRM API, this operation is `GET /tasks/` (base URL `https://api.okocrm.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tasks.md) for the provider-specific parameters and requirements.

