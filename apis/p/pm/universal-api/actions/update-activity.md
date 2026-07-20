# 5pm: Update Activity

Updates an existing activity in 5pm.

```
PUT https://connect.mindcloud.co/v1/universal/pm/latest/actions/update-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 5pm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pm/latest/actions/update-activity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "activity.id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pm/latest/actions/update-activity', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "activity.id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `activity.id` | string | yes | Unique identifier of the activity. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "ownerId": 1,
      "progress": 1,
      "projectId": 1,
      "taskId": 1,
      "text": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | date | Activity posting date. |
| `id` | string | Activity identifier. |
| `ownerId` | number | Activity owner user ID. |
| `progress` | number | Activity progress percentage. |
| `projectId` | number | Related project ID. |
| `taskId` | number | Related task ID. |
| `text` | string | Activity text. |
| `type` | string | Activity type. |

## Native endpoint

Through the native 5pm API, this operation is `POST /service/post/activity/update` (base URL `{{credentials.workspaceUrl}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-activity.md) for the provider-specific parameters and requirements.

