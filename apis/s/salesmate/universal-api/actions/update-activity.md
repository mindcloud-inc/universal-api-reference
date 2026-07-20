# Salesmate: Update Activity



```
PUT https://connect.mindcloud.co/v1/universal/salesmate/latest/actions/update-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salesmate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/salesmate/latest/actions/update-activity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "activityId": 1,
  "title": "string",
  "owner": 1,
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/salesmate/latest/actions/update-activity', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "activityId": 1,
    "title": "string",
    "owner": 1,
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `activityId` | number | yes | Salesmate activity ID. |
| `title` | string | yes | Activity title. |
| `owner` | number | yes | Salesmate user ID that owns the activity. |
| `type` | string | yes | Activity type such as Call or Meeting. |
| `dueDate` | date | no | Activity due date/time. |
| `description` | string | no | Internal activity description. |
| `duration` | number | no | Activity duration in minutes. |
| `primaryContact` | number | no | Primary contact linked to the activity. |
| `tags` | string | no | Comma-separated tag list. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `isCalendarInvite` | boolean | no | Whether Salesmate should send a calendar invite. Default: `false`. |
| `isCompleted` | boolean | no | Whether the activity is already completed. Default: `false`. |
| `followers[]` | array<object> | no | Follower objects such as { userId } or { contactId }. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Salesmate API, this operation is `PUT /activity/v4/:activityId` (base URL `https://apis.salesmate.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-activity.md) for the provider-specific parameters and requirements.

