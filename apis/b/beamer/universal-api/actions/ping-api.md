# Beamer: Ping API

Pings the Beamer API to verify connectivity.

```
POST https://connect.mindcloud.co/v1/universal/beamer/latest/actions/ping-api
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Beamer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/beamer/latest/actions/ping-api" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/beamer/latest/actions/ping-api', {
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

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Beamer API returns.

## Native endpoint

Through the native Beamer API, this operation is `POST /v0/ping` (base URL `https://api.getbeamer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/ping-api.md) for the provider-specific parameters and requirements.

