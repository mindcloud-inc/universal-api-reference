# Zixflow: Update Activity

Updates an existing activity in Zixflow.

```
PUT https://connect.mindcloud.co/v1/universal/zixflow/latest/actions/update-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zixflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zixflow/latest/actions/update-activity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "activityId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zixflow/latest/actions/update-activity', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "activityId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `activityId` | string | yes | Activity identifier. |
| `iconType` | string | no | Activity icon type. |
| `iconValue` | string | no | Activity icon value. |
| `name` | string | no | Activity name. |
| `scheduleAt` | string | no | Scheduled timestamp for the activity. |
| `description` | string | no | Activity description. |
| `associated` | string | no | Associated record reference. |
| `status` | string | no | Activity status identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string",
      "status": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Updated activity payload returned by Zixflow. |
| `message` | string | Provider success or error message. |
| `status` | boolean | Whether the activity update request succeeded. |

## Native endpoint

Through the native Zixflow API, this operation is `PATCH /collection-records/activity-list/:activityId` (base URL `https://api.zixflow.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-activity.md) for the provider-specific parameters and requirements.

