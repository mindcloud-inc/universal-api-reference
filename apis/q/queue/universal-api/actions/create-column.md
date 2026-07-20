# Queue: Create Column

Creates a new column for a Queue project.

```
POST https://connect.mindcloud.co/v1/universal/queue/latest/actions/create-column
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Queue `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/queue/latest/actions/create-column" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/queue/latest/actions/create-column', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | Required path parameter from projects/:project_id/columns. |
| `title` | string | no | The title of the column |
| `position` | number | no | The column's position (0-indexed) within the project |
| `stage` | string | no | The internal stage type of the column. Can be 'in_queue', 'in_progress', or 'done' |
| `finished` | boolean | no | Whether tasks in this column are marked as finished |
| `startTimer` | boolean | no | Whether tasks in this column should start the timer automatically |

## Response

```json
{
  "success": true,
  "data": [
    {
      "finished": true,
      "id": "string",
      "position": 1,
      "stage": "string",
      "startTimer": true,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `finished` | boolean |  |
| `id` | string |  |
| `position` | number |  |
| `stage` | string |  |
| `startTimer` | boolean |  |
| `title` | string |  |

## Native endpoint

Through the native Queue API, this operation is `POST projects/:project_id/columns` (base URL `https://app.usequeue.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-column.md) for the provider-specific parameters and requirements.

