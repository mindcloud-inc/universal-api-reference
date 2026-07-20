# GatherUp: Auto Feedback Requests

Updates auto feedback request settings in GatherUp.

```
PUT https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/auto-feedback-requests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GatherUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/auto-feedback-requests" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "businessId": 1,
  "autoFeedback": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/auto-feedback-requests', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "businessId": 1,
    "autoFeedback": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `businessId` | number | yes | Business id. |
| `autoFeedback` | number | yes | 1 = Automatic Mode \| 0 = Manual Mode |
| `autoSend` | number | no | Amount of feedbacks per day in Automatic Mode |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GatherUp API returns.

## Native endpoint

Through the native GatherUp API, this operation is `POST /business/auto-feedback-requests` (base URL `https://app.gatherup.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/auto-feedback-requests.md) for the provider-specific parameters and requirements.

