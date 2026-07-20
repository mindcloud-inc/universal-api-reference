# Trello: Add Comment to Card

Creates a comment on a Trello card.

```
POST https://connect.mindcloud.co/v1/universal/trello/latest/actions/add-comment-to-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trello `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/trello/latest/actions/add-comment-to-card" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trello/latest/actions/add-comment-to-card', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Card identifier. |
| `text` | string | yes | Comment text to add to the card. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "string",
      "id": "string",
      "idMemberCreator": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | string |  |
| `id` | string |  |
| `idMemberCreator` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Trello API, this operation is `POST cards/:id/actions/comments` (base URL `https://api.trello.com/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-comment-to-card.md) for the provider-specific parameters and requirements.

