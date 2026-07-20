# Strale: Execute Task

Executes a task in Strale using semantic matching.

```
POST https://connect.mindcloud.co/v1/universal/strale/latest/actions/execute-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Strale `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/strale/latest/actions/execute-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "task": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/strale/latest/actions/execute-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "task": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dry_run` | boolean | no | Return the matched capability without executing it. |
| `max_price_cents` | number | no | Maximum price you are willing to pay in euro cents. |
| `min_sqs` | number | no | Minimum acceptable Strale Quality Score. |
| `task` | string | yes | Natural language task to execute. |
| `timeout_seconds` | number | no | Maximum execution time in seconds. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dryRun": true,
      "priceCents": 1,
      "walletBalanceCents": 1,
      "walletSufficient": true,
      "wouldExecute": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dryRun` | boolean | Whether the result is a dry-run preview. |
| `priceCents` | number | Estimated execution price in cents. |
| `walletBalanceCents` | number | Current wallet balance in cents. |
| `walletSufficient` | boolean | Whether the wallet can cover the estimated cost. |
| `wouldExecute` | string | Capability slug that would run. |

## Native endpoint

Through the native Strale API, this operation is `POST /v1/do` (base URL `https://api.strale.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/execute-task.md) for the provider-specific parameters and requirements.

