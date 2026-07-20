# IgniSign: Revoke Signer



```
DELETE https://connect.mindcloud.co/v1/universal/igniSign/latest/actions/revoke-signer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IgniSign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/igniSign/latest/actions/revoke-signer?connectionId=$CONNECTION_ID&signerId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "signerId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/igniSign/latest/actions/revoke-signer?${params}`, {
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
| `signerId` | string | yes | The IgniSign signer ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "signerId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `signerId` | string |  |

## Native endpoint

Through the native IgniSign API, this operation is `DELETE /v4/applications/:appId/envs/:appEnv/signers/:signerId/revoke` (base URL `https://api.ignisign.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/revoke-signer.md) for the provider-specific parameters and requirements.

