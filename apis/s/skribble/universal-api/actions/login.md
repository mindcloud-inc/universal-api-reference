# Skribble: Login

Creates an API access token in Skribble.

```
POST https://connect.mindcloud.co/v1/universal/skribble/latest/actions/login
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Skribble `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/skribble/latest/actions/login" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/skribble/latest/actions/login', {
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

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Skribble API returns.

## Native endpoint

Through the native Skribble API, this operation is `POST /v2/access/login` (base URL `https://api.skribble.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/login.md) for the provider-specific parameters and requirements.

