# SuperSend: Update Conversation

Updates an existing conversation in SuperSend.

```
PUT https://connect.mindcloud.co/v1/universal/superSend/latest/actions/update-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperSend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/superSend/latest/actions/update-conversation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/superSend/latest/actions/update-conversation', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |
| `isArchived` | boolean | no |  |
| `isUnread` | boolean | no |  |
| `markAllRead` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "is_archived": true,
      "is_unread": true,
      "object": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `is_archived` | boolean |  |
| `is_unread` | boolean |  |
| `object` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native SuperSend API, this operation is `PATCH /conversations/{id}` (base URL `https://api.supersend.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-conversation.md) for the provider-specific parameters and requirements.

