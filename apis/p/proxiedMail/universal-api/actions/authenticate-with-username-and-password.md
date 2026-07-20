# ProxiedMail: Authenticate With Username And Password



```
POST https://connect.mindcloud.co/v1/universal/proxiedMail/latest/actions/authenticate-with-username-and-password
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProxiedMail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/proxiedMail/latest/actions/authenticate-with-username-and-password" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "username": "apps@mindcloud.co",
  "password": "account password"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/proxiedMail/latest/actions/authenticate-with-username-and-password', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "username": "apps@mindcloud.co",
    "password": "account password"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `username` | string | yes | Example: `apps@mindcloud.co`. |
| `password` | string | yes | Example: `account password`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ProxiedMail API returns.

## Native endpoint

Through the native ProxiedMail API, this operation is `POST /auth` (base URL `https://proxiedmail.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/authenticate-with-username-and-password.md) for the provider-specific parameters and requirements.

