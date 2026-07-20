# Miro: Share Board

Shares a board with a member in Miro.

```
POST https://connect.mindcloud.co/v1/universal/miro/latest/actions/share-board
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Miro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/miro/latest/actions/share-board" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/miro/latest/actions/share-board', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `boardId` | string | no | Target board ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "failed": [
        {
          "email": "ava@example.com",
          "reason": "string"
        }
      ],
      "successful": [
        1
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `failed[].email` | string |  |
| `failed[].reason` | string |  |
| `successful` | array<number> |  |

## Native endpoint

Through the native Miro API, this operation is `POST /boards/:board_id/members` (base URL `https://api.miro.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/share-board.md) for the provider-specific parameters and requirements.

