# Platrum: List board tasks

Retrieves tasks from a Platrum board.

```
GET https://connect.mindcloud.co/v1/universal/platrum/latest/actions/list-board-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Platrum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/platrum/latest/actions/list-board-tasks?connectionId=$CONNECTION_ID&board_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "board_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/platrum/latest/actions/list-board-tasks?${params}`, {
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
| `board_id` | number | yes | Board ID to list tasks for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `status` | string |  |

## Native endpoint

Through the native Platrum API, this operation is `POST /tasks/api/board/task/list` (base URL `https://3e8e7be.platrum.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-board-tasks.md) for the provider-specific parameters and requirements.

