# Kanban Zone: List Card Comments

Retrieves comments for a Kanban Zone card.

```
GET https://connect.mindcloud.co/v1/universal/kanbanZone/latest/actions/list-card-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kanban Zone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kanbanZone/latest/actions/list-card-comments?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kanbanZone/latest/actions/list-card-comments?${params}`, {
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
| `id` | number | yes | The unique identifier of the card. |

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

Through the native Kanban Zone API, this operation is `GET /cards/:id/comments` (base URL `https://integrations.kanbanzone.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-card-comments.md) for the provider-specific parameters and requirements.

