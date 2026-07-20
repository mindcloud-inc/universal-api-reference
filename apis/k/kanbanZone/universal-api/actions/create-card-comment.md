# Kanban Zone: Create Card Comment

Creates a card comment in Kanban Zone.

```
POST https://connect.mindcloud.co/v1/universal/kanbanZone/latest/actions/create-card-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kanban Zone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kanbanZone/latest/actions/create-card-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kanbanZone/latest/actions/create-card-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The unique identifier of the card |
| `text` | string | yes | The content of the comment |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "author": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "plainText": "string",
      "reactions": [
        {}
      ],
      "replies": [
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
| `_id` | string |  |
| `author` | string |  |
| `createdAt` | date |  |
| `plainText` | string |  |
| `reactions` | array<object> |  |
| `replies` | array<object> |  |

## Native endpoint

Through the native Kanban Zone API, this operation is `POST /cards/:id/comments` (base URL `https://integrations.kanbanzone.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-card-comment.md) for the provider-specific parameters and requirements.

