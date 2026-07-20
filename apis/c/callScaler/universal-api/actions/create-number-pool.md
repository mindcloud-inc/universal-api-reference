# CallScaler: Create Number Pool

Creates a number pool in CallScaler.

```
POST https://connect.mindcloud.co/v1/universal/callScaler/latest/actions/create-number-pool
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallScaler `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/callScaler/latest/actions/create-number-pool" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/callScaler/latest/actions/create-number-pool', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native CallScaler API returns.

## Native endpoint

Through the native CallScaler API, this operation is `POST /number-pools` (base URL `https://callscaler.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-number-pool.md) for the provider-specific parameters and requirements.

