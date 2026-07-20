# IgniSign: Create Signer



```
POST https://connect.mindcloud.co/v1/universal/igniSign/latest/actions/create-signer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IgniSign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/igniSign/latest/actions/create-signer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/igniSign/latest/actions/create-signer', {
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

```json
{
  "success": true,
  "data": [
    {
      "alreadyExists": true,
      "authSecret": "string",
      "entityType": "string",
      "signerId": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alreadyExists` | boolean | Whether the signer already existed. |
| `authSecret` | string | The generated signer authentication secret. |
| `entityType` | string | The signer entity type. |
| `signerId` | string | The created signer identifier. |
| `success` | boolean | Whether the signer creation succeeded. |

## Native endpoint

Through the native IgniSign API, this operation is `POST /v4/applications/:appId/envs/:appEnv/signers` (base URL `https://api.ignisign.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-signer.md) for the provider-specific parameters and requirements.

