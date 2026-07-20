# KanbanFlow: Get board time entries

Retrieves board time entries from KanbanFlow for a time period.

```
GET https://connect.mindcloud.co/v1/universal/kanbanFlow/latest/actions/get-board-time-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KanbanFlow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kanbanFlow/latest/actions/get-board-time-entries?connectionId=$CONNECTION_ID&from=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "from": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kanbanFlow/latest/actions/get-board-time-entries?${params}`, {
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
| `from` | string | yes | Include time entries that start or end after this UTC timestamp. |
| `to` | string | no | Include time entries that start or end before this UTC timestamp. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comment": "string",
      "endTimestamp": "string",
      "entryId": "string",
      "startTimestamp": "string",
      "taskId": "string",
      "type": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comment` | string |  |
| `endTimestamp` | string |  |
| `entryId` | string |  |
| `startTimestamp` | string |  |
| `taskId` | string |  |
| `type` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native KanbanFlow API, this operation is `GET /time-entries` (base URL `https://kanbanflow.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-board-time-entries.md) for the provider-specific parameters and requirements.

