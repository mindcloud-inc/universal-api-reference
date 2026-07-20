# Logit: Restart Stack Pipeline

Restarts a stack pipeline in Logit.

```
PUT https://connect.mindcloud.co/v1/universal/logit/latest/actions/restart-stack-pipeline
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Logit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/logit/latest/actions/restart-stack-pipeline" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "stackId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/logit/latest/actions/restart-stack-pipeline', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "stackId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `stackId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Logit API returns.

## Native endpoint

Through the native Logit API, this operation is `POST /api/stacks/:stackId/pipeline/restart` (base URL `https://dashboard.logit.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/restart-stack-pipeline.md) for the provider-specific parameters and requirements.

