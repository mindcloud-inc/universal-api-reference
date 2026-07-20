# ZAP POST: Create Single Record Submission Valid Records Only

Creates a single-record submission using only valid records.

```
POST https://connect.mindcloud.co/v1/universal/zAPPOST/latest/actions/create-single-record-submission-valid-records-only
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ZAP POST `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zAPPOST/latest/actions/create-single-record-submission-valid-records-only" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": "string",
  "submissions[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zAPPOST/latest/actions/create-single-record-submission-valid-records-only', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": "string",
    "submissions[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignId` | string | yes | The campaign UUID to submit the record against. |
| `submissions[]` | array<object> | yes | Provide a single submission record in the array for the /records endpoint. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ZAP POST API returns.

## Native endpoint

Through the native ZAP POST API, this operation is `POST /api/v1/records` (base URL `https://api.zappost.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-single-record-submission-valid-records-only.md) for the provider-specific parameters and requirements.

