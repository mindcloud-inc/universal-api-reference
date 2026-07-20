# Vector Vault: Authenticate



```
POST https://connect.mindcloud.co/v1/universal/vectorVault/latest/actions/authenticate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vector Vault `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vectorVault/latest/actions/authenticate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "{{credentials.email}}",
  "apiKey": "{{credentials.apiKey}}"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vectorVault/latest/actions/authenticate', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "{{credentials.email}}",
    "apiKey": "{{credentials.apiKey}}"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | The Vector Vault account email. Default: `{{credentials.email}}`. |
| `apiKey` | string | yes | The Vector Vault API key. Default: `{{credentials.apiKey}}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "access_token": "string",
      "refresh_token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access_token` | string |  |
| `refresh_token` | string |  |

## Native endpoint

Through the native Vector Vault API, this operation is `POST login_with_api` (base URL `https://api.vectorvault.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/authenticate.md) for the provider-specific parameters and requirements.

