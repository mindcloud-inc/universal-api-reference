# Zoho Connect: Create Board

Creates a new board in Zoho Connect.

```
POST https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/create-board
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Connect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/create-board" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "desc": "string",
  "name": "Ava Chen",
  "scopeID": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/create-board', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "desc": "string",
    "name": "Ava Chen",
    "scopeID": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `desc` | string | yes | Description for the board. |
| `memberIds` | string | no | Comma-separated Zoho user IDs to add to the board. Accepts multiple values in one string, delimited by `,`. |
| `name` | string | yes | Name of the board to create. |
| `scopeID` | string | yes | ID of the network where the board will be created. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addBoard": {
        "board": {
          "id": "string",
          "isAdmin": true,
          "name": "Ava Chen",
          "status": "string",
          "type": "string",
          "url": "https://example.com"
        },
        "members": [
          {}
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addBoard.board.id` | string |  |
| `addBoard.board.isAdmin` | boolean |  |
| `addBoard.board.name` | string |  |
| `addBoard.board.status` | string |  |
| `addBoard.board.type` | string |  |
| `addBoard.board.url` | string |  |
| `addBoard.members` | array<object> |  |

## Native endpoint

Through the native Zoho Connect API, this operation is `POST /pulse/api/addBoard` (base URL `https://connect.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-board.md) for the provider-specific parameters and requirements.

