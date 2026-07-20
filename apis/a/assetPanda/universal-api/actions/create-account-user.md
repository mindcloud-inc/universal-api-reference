# Asset Panda: Create Account User

Creates a new user account in Asset Panda.

```
POST https://connect.mindcloud.co/v1/universal/assetPanda/latest/actions/create-account-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Asset Panda `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/assetPanda/latest/actions/create-account-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/assetPanda/latest/actions/create-account-user', {
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

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Asset Panda API returns.

## Native endpoint

Through the native Asset Panda API, this operation is `POST /v3/accounts` (base URL `https://api.assetpanda.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-account-user.md) for the provider-specific parameters and requirements.

