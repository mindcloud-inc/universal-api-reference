# ActivitySmith: Start Live Activity

Creates a Live Activity in ActivitySmith.

```
POST https://connect.mindcloud.co/v1/universal/activitySmith/latest/actions/start-live-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ActivitySmith `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/activitySmith/latest/actions/start-live-activity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contentState": {},
  "contentState.title": "string",
  "contentState.type": "string",
  "contentState.numberOfSteps": 1,
  "contentState.currentStep": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/activitySmith/latest/actions/start-live-activity', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contentState": {},
    "contentState.title": "string",
    "contentState.type": "string",
    "contentState.numberOfSteps": 1,
    "contentState.currentStep": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contentState` | object | yes |  |
| `contentState.title` | string | yes |  |
| `contentState.type` | string | yes |  |
| `contentState.numberOfSteps` | number | yes |  |
| `contentState.currentStep` | number | yes |  |
| `contentState.subtitle` | string | no |  |
| `contentState.color` | string | no |  |
| `target` | object | no |  |
| `target.channels[]` | array<string> | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ActivitySmith API returns.

## Native endpoint

Through the native ActivitySmith API, this operation is `POST /live-activity/start` (base URL `https://activitysmith.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-live-activity.md) for the provider-specific parameters and requirements.

