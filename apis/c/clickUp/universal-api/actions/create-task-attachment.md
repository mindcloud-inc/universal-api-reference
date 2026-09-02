# ClickUp: Create Task Attachment

Uploads a file attachment to a ClickUp task.

```
POST https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/create-task-attachment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/create-task-attachment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": "string",
  "attachment": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/create-task-attachment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskId": "string",
    "attachment": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customTaskIds` | boolean | no |  |
| `taskId` | string | yes |  |
| `teamId` | list | no |  |
| `attachment` | file | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": 1,
      "extension": "string",
      "id": "string",
      "thumbnailLarge": "string",
      "thumbnailSmall": "string",
      "title": "string",
      "url": "https://example.com",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | number |  |
| `extension` | string |  |
| `id` | string |  |
| `thumbnailLarge` | string |  |
| `thumbnailSmall` | string |  |
| `title` | string |  |
| `url` | string |  |
| `version` | string |  |

## Native endpoint

Through the native ClickUp API, this operation is `POST task/:task_id/attachment` (base URL `https://api.clickup.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task-attachment.md) for the provider-specific parameters and requirements.

