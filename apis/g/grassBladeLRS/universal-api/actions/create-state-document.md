# GrassBlade LRS: Create State Document

Stores or updates a state document in GrassBlade LRS.

```
POST https://connect.mindcloud.co/v1/universal/grassBladeLRS/latest/actions/create-state-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrassBlade LRS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/grassBladeLRS/latest/actions/create-state-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "activityId": "https://mindcloud.dev/grassblade/activity/stage3-20260406",
  "agent": "[object Object]",
  "stateId": "mindcloud-state-stage3",
  "document": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/grassBladeLRS/latest/actions/create-state-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "activityId": "https://mindcloud.dev/grassblade/activity/stage3-20260406",
    "agent": "[object Object]",
    "stateId": "mindcloud-state-stage3",
    "document": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `activityId` | string | yes | Example: `https://mindcloud.dev/grassblade/activity/stage3-20260406`. |
| `agent` | string | yes | Example: `[object Object]`. |
| `stateId` | string | yes | Example: `mindcloud-state-stage3`. |
| `document` | object | yes | Example: `[object Object]`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `registration` | string | no | Example: `7d1e5c30-1a57-4b72-bf87-23e7fd355f90`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GrassBlade LRS API returns.

## Native endpoint

Through the native GrassBlade LRS API, this operation is `POST /activities/state` (base URL `https://test.gblrs.com/xAPI`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-state-document.md) for the provider-specific parameters and requirements.

