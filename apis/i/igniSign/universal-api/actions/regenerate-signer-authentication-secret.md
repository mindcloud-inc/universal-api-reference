# IgniSign: Regenerate Signer Authentication Secret



```
PUT https://connect.mindcloud.co/v1/universal/igniSign/latest/actions/regenerate-signer-authentication-secret
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IgniSign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/igniSign/latest/actions/regenerate-signer-authentication-secret" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "signerId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/igniSign/latest/actions/regenerate-signer-authentication-secret', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "signerId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `signerId` | string | yes | The IgniSign signer ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authSecret": "string",
      "signerId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authSecret` | string |  |
| `signerId` | string |  |

## Native endpoint

Through the native IgniSign API, this operation is `PUT /v4/applications/:appId/envs/:appEnv/signers/:signerId/regenerate-auth-secret` (base URL `https://api.ignisign.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/regenerate-signer-authentication-secret.md) for the provider-specific parameters and requirements.

