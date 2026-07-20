# Infisical: Authenticate

Authenticates with Infisical using Universal Auth.

```
POST https://connect.mindcloud.co/v1/universal/infisical/latest/actions/authenticate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Infisical `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/infisical/latest/actions/authenticate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "clientId": "{{credentials.clientId}}",
  "clientSecret": "{{credentials.clientSecret}}"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/infisical/latest/actions/authenticate', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "clientId": "{{credentials.clientId}}",
    "clientSecret": "{{credentials.clientSecret}}"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clientId` | string | yes | The Infisical machine identity Client ID. Default: `{{credentials.clientId}}`. |
| `clientSecret` | string | yes | The Infisical machine identity Client Secret. Default: `{{credentials.clientSecret}}`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Infisical API returns.

## Native endpoint

Through the native Infisical API, this operation is `POST /api/v1/auth/universal-auth/login` (base URL `https://app.infisical.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/authenticate.md) for the provider-specific parameters and requirements.

