# GanttPRO: Update Task Comment

Updates an existing task comment in GanttPRO.

```
PUT https://connect.mindcloud.co/v1/universal/ganttPRO/latest/actions/update-task-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GanttPRO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ganttPRO/latest/actions/update-task-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "commentId": 1,
  "content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ganttPRO/latest/actions/update-task-comment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "commentId": 1,
    "content": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `commentId` | number | yes | GanttPRO comment identifier. |
| `content` | string | yes | Updated comment content. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string |  |

## Native endpoint

Through the native GanttPRO API, this operation is `PUT /comments/:commentId` (base URL `https://api.ganttpro.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task-comment.md) for the provider-specific parameters and requirements.

