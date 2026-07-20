# IgniSign: Initialize Signature Request



```
POST https://connect.mindcloud.co/v1/universal/igniSign/latest/actions/initialize-signature-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IgniSign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/igniSign/latest/actions/initialize-signature-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/igniSign/latest/actions/initialize-signature-request', {
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
      "_id": "string",
      "appEnv": "string",
      "appId": "string",
      "signatureRequestType": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `appEnv` | string |  |
| `appId` | string |  |
| `signatureRequestType` | string |  |
| `status` | string |  |

## Native endpoint

Through the native IgniSign API, this operation is `POST /v4/applications/:appId/envs/:appEnv/signature-requests` (base URL `https://api.ignisign.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/initialize-signature-request.md) for the provider-specific parameters and requirements.

