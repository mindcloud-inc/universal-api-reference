# Whattime: Create Routing Form



```
POST https://connect.mindcloud.co/v1/universal/whattime/latest/actions/create-routing-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Whattime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/whattime/latest/actions/create-routing-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/whattime/latest/actions/create-routing-form', {
  method: 'POST',
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
      "code": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "uri": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `created_at` | date |  |
| `name` | string |  |
| `updated_at` | date |  |
| `uri` | string |  |

## Native endpoint

Through the native Whattime API, this operation is `POST /routing_forms` (base URL `https://api.whattime.co.kr/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-routing-form.md) for the provider-specific parameters and requirements.

