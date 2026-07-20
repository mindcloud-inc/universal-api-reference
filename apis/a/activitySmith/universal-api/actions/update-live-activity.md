# ActivitySmith: Update Live Activity

Updates an existing Live Activity in ActivitySmith.

```
PUT https://connect.mindcloud.co/v1/universal/activitySmith/latest/actions/update-live-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ActivitySmith `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/activitySmith/latest/actions/update-live-activity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "activityId": "string",
  "contentState": {},
  "contentState.title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/activitySmith/latest/actions/update-live-activity', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "activityId": "string",
    "contentState": {},
    "contentState.title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `activityId` | string | yes |  |
| `contentState` | object | yes |  |
| `contentState.title` | string | yes |  |
| `contentState.type` | string | no |  |
| `contentState.numberOfSteps` | number | no |  |
| `contentState.currentStep` | number | no |  |
| `contentState.subtitle` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ActivitySmith API returns.

## Native endpoint

Through the native ActivitySmith API, this operation is `POST /live-activity/update` (base URL `https://activitysmith.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-live-activity.md) for the provider-specific parameters and requirements.

