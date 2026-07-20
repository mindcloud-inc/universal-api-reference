# Zixflow: Create Activity

Creates a new activity in Zixflow.

```
POST https://connect.mindcloud.co/v1/universal/zixflow/latest/actions/create-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zixflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zixflow/latest/actions/create-activity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "iconType": "string",
  "iconValue": "string",
  "name": "Ava Chen",
  "scheduleAt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zixflow/latest/actions/create-activity', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "iconType": "string",
    "iconValue": "string",
    "name": "Ava Chen",
    "scheduleAt": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `iconType` | string | yes | Activity icon type. |
| `iconValue` | string | yes | Activity icon value. |
| `name` | string | yes | Activity name. |
| `scheduleAt` | string | yes | Scheduled timestamp for the activity. |
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
| `data` | object | Created activity payload returned by Zixflow. |
| `message` | string | Provider success or error message. |
| `status` | boolean | Whether the activity create request succeeded. |

## Native endpoint

Through the native Zixflow API, this operation is `POST /collection-records/activity-list` (base URL `https://api.zixflow.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-activity.md) for the provider-specific parameters and requirements.

