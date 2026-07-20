# KanbanFlow: Get board

Retrieves the structure of a KanbanFlow board.

```
GET https://connect.mindcloud.co/v1/universal/kanbanFlow/latest/actions/get-board
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KanbanFlow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kanbanFlow/latest/actions/get-board?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kanbanFlow/latest/actions/get-board?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "colors": [
        {
          "name": "Ava Chen",
          "value": "string"
        }
      ],
      "columns": [
        {
          "name": "Ava Chen",
          "uniqueId": "string"
        }
      ],
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `colors` | array<object> |  |
| `colors[].name` | string |  |
| `colors[].value` | string |  |
| `columns` | array<object> |  |
| `columns[].name` | string |  |
| `columns[].uniqueId` | string |  |
| `name` | string |  |

## Native endpoint

Through the native KanbanFlow API, this operation is `GET /board` (base URL `https://kanbanflow.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-board.md) for the provider-specific parameters and requirements.

