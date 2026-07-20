# Seqera: Cancel Run

Cancels a workflow run in Seqera.

```
PUT https://connect.mindcloud.co/v1/universal/seqera/latest/actions/cancel-run
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seqera `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/seqera/latest/actions/cancel-run" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "run_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/seqera/latest/actions/cancel-run', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "run_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `run_id` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Seqera API returns.

## Native endpoint

Through the native Seqera API, this operation is `POST /ga4gh/wes/v1/runs/:run_id/cancel` (base URL `https://api.cloud.seqera.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-run.md) for the provider-specific parameters and requirements.

