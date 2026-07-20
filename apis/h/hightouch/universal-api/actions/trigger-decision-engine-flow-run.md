# Hightouch: Trigger Decision Engine Flow Run

Triggers a decision engine flow run in Hightouch.

```
POST https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/trigger-decision-engine-flow-run
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hightouch `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/trigger-decision-engine-flow-run" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "flowId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/trigger-decision-engine-flow-run', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "flowId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `flowId` | string | yes | The Decision Engine flow ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "flowsEnqueued": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `flowsEnqueued` | number | Number of flows enqueued for execution. |

## Native endpoint

Through the native Hightouch API, this operation is `POST /decision-engine/flow/{flowId}/run` (base URL `https://api.hightouch.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/trigger-decision-engine-flow-run.md) for the provider-specific parameters and requirements.

