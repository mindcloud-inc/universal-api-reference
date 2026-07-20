# SMASHSEND Email Marketing: Track Events Batch

Tracks multiple contact events in SMASHSEND in one batch.

```
POST https://connect.mindcloud.co/v1/universal/sMASHSENDEmailMarketing/latest/actions/track-events-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMASHSEND Email Marketing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sMASHSENDEmailMarketing/latest/actions/track-events-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "events[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sMASHSENDEmailMarketing/latest/actions/track-events-batch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "events[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `events[]` | array<object> | yes | Array of event payloads to send in a single batch request. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SMASHSEND Email Marketing API returns.

## Native endpoint

Through the native SMASHSEND Email Marketing API, this operation is `POST /v1/events/batch` (base URL `https://api.smashsend.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/track-events-batch.md) for the provider-specific parameters and requirements.

