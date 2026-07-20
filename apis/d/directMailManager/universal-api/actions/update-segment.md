# Direct Mail Manager: Update Segment



```
PUT https://connect.mindcloud.co/v1/universal/directMailManager/latest/actions/update-segment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Direct Mail Manager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/directMailManager/latest/actions/update-segment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/directMailManager/latest/actions/update-segment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "conditions": [
        {}
      ],
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "object": "string",
      "total": 1,
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `conditions` | array<object> |  |
| `created_at` | date |  |
| `id` | string |  |
| `name` | string |  |
| `object` | string |  |
| `total` | number |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Direct Mail Manager API, this operation is `PUT /segments/:sgm_id` (base URL `https://api.directmailmanager.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-segment.md) for the provider-specific parameters and requirements.

