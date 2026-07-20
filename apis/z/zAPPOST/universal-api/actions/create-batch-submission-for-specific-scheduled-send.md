# ZAP POST: Create Batch Submission For Specific Scheduled Send

Creates a batch submission for a specific scheduled send.

```
POST https://connect.mindcloud.co/v1/universal/zAPPOST/latest/actions/create-batch-submission-for-specific-scheduled-send
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ZAP POST `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zAPPOST/latest/actions/create-batch-submission-for-specific-scheduled-send" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": "string",
  "scheduledSendDateId": "string",
  "submissions[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zAPPOST/latest/actions/create-batch-submission-for-specific-scheduled-send', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": "string",
    "scheduledSendDateId": "string",
    "submissions[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignId` | string | yes | The campaign UUID to submit the records against. |
| `scheduledSendDateId` | string | yes | The specific scheduled send UUID to use. |
| `submissions[]` | array<object> | yes | Provide one or more submission records in the array for the /submissions endpoint. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ZAP POST API returns.

## Native endpoint

Through the native ZAP POST API, this operation is `POST /api/v1/submissions` (base URL `https://api.zappost.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-batch-submission-for-specific-scheduled-send.md) for the provider-specific parameters and requirements.

