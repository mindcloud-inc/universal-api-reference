# Pachca: Update message



```
PUT https://connect.mindcloud.co/v1/universal/pachca/latest/actions/update-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pachca `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pachca/latest/actions/update-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "message": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pachca/latest/actions/update-message', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "message": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Pachca message ID. |
| `message` | object | yes | Message parameters object. |
| `message.content` | string | no | Message text. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "chat_id": 1,
      "content": "string",
      "id": 1,
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
| `chat_id` | number |  |
| `content` | string |  |
| `id` | number |  |
| `updated_at` | date |  |
| `url` | string |  |
| `user_id` | number |  |

## Native endpoint

Through the native Pachca API, this operation is `PUT /messages/{id}` (base URL `https://api.pachca.com/api/shared/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-message.md) for the provider-specific parameters and requirements.

