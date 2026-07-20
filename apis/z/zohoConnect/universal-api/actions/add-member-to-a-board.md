# Zoho Connect: Add Member to a Board

Adds members to a board in Zoho Connect.

```
POST https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/add-member-to-a-board
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Connect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/add-member-to-a-board" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "boardId": "string",
  "memberIds": "string",
  "scopeID": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/add-member-to-a-board', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "boardId": "string",
    "memberIds": "string",
    "scopeID": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `boardId` | string | yes | ID of the board to add members to. |
| `memberIds` | string | yes | Comma-separated user IDs to add to the board. Accepts multiple values in one string, delimited by `,`. |
| `scopeID` | string | yes | ID of the network that contains the board. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addMembersToBoard": {
        "reason": "string",
        "result": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addMembersToBoard.reason` | string |  |
| `addMembersToBoard.result` | string |  |

## Native endpoint

Through the native Zoho Connect API, this operation is `POST /pulse/api/addMembersToBoard` (base URL `https://connect.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-member-to-a-board.md) for the provider-specific parameters and requirements.

