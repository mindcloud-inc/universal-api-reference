# IgniSign: Get Signer Input Constraints



```
GET https://connect.mindcloud.co/v1/universal/igniSign/latest/actions/get-signer-input-constraints
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IgniSign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/igniSign/latest/actions/get-signer-input-constraints?connectionId=$CONNECTION_ID&signerProfileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "signerProfileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/igniSign/latest/actions/get-signer-input-constraints?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `signerProfileId` | string | yes | The IgniSign signer profile ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "constraints": {},
      "inputs": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `constraints` | object |  |
| `inputs` | array<object> |  |

## Native endpoint

Through the native IgniSign API, this operation is `GET /v4/applications/:appId/envs/:appEnv/signer-profiles/:signerProfileId/inputs-needed` (base URL `https://api.ignisign.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-signer-input-constraints.md) for the provider-specific parameters and requirements.

