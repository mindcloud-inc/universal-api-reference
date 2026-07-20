# Zoho Connect: Get Board Sections

Retrieves board sections from Zoho Connect.

```
GET https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/get-board-sections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Connect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/get-board-sections?connectionId=$CONNECTION_ID&boardId=string&scopeID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "boardId": "string",
  "scopeID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/get-board-sections?${params}`, {
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
| `boardId` | string | yes | ID of the board to return sections for. |
| `scopeID` | string | yes | ID of the network that contains the board. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "boardSections": {
        "board": {
          "desc": "string",
          "id": "string",
          "name": "Ava Chen",
          "status": "string"
        },
        "canEditPartition": true,
        "members": [
          {}
        ],
        "stats": {
          "activeTasks": 1,
          "completedTasks": 1,
          "overdueTasks": 1
        },
        "tags": [
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
| `boardSections.board.desc` | string |  |
| `boardSections.board.id` | string |  |
| `boardSections.board.name` | string |  |
| `boardSections.board.status` | string |  |
| `boardSections.canEditPartition` | boolean |  |
| `boardSections.members` | array<object> |  |
| `boardSections.stats.activeTasks` | number |  |
| `boardSections.stats.completedTasks` | number |  |
| `boardSections.stats.overdueTasks` | number |  |
| `boardSections.tags` | array<object> |  |

## Native endpoint

Through the native Zoho Connect API, this operation is `GET /pulse/api/boardSections` (base URL `https://connect.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-board-sections.md) for the provider-specific parameters and requirements.

