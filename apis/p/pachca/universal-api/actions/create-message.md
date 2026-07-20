# Pachca: Create message



```
POST https://connect.mindcloud.co/v1/universal/pachca/latest/actions/create-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pachca `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pachca/latest/actions/create-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "message": {},
  "message.entity_id": 1,
  "message.content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pachca/latest/actions/create-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "message": {},
    "message.entity_id": 1,
    "message.content": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `message` | object | yes | Message parameters object. |
| `message.entity_id` | number | yes | Target chat/thread entity ID. |
| `message.entity_type` | string | no | Entity type. Defaults to discussion. Default: `discussion`. |
| `message.content` | string | yes | Message text. |
| `link_preview` | boolean | no | Whether to display a link preview. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "chat_id": 1,
      "content": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "files": [
        {}
      ],
      "id": 1,
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
| `created_at` | date |  |
| `files` | array<object> |  |
| `id` | number |  |
| `url` | string |  |
| `user_id` | number |  |

## Native endpoint

Through the native Pachca API, this operation is `POST /messages` (base URL `https://api.pachca.com/api/shared/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-message.md) for the provider-specific parameters and requirements.

