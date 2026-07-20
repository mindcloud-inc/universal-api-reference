# Quiltt: Create Straddle Processor Token



```
POST https://connect.mindcloud.co/v1/universal/quiltt/latest/actions/create-straddle-processor-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quiltt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/quiltt/latest/actions/create-straddle-processor-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quiltt/latest/actions/create-straddle-processor-token', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | string | yes | Quiltt account ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Quiltt API returns.

## Native endpoint

Through the native Quiltt API, this operation is `POST /v1/accounts/:accountId/processor_tokens` (base URL `https://api.quiltt.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-straddle-processor-token.md) for the provider-specific parameters and requirements.

