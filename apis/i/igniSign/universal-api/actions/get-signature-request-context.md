# IgniSign: Get Signature Request Context



```
GET https://connect.mindcloud.co/v1/universal/igniSign/latest/actions/get-signature-request-context
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IgniSign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/igniSign/latest/actions/get-signature-request-context?connectionId=$CONNECTION_ID&signatureRequestId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "signatureRequestId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/igniSign/latest/actions/get-signature-request-context?${params}`, {
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
| `signatureRequestId` | string | yes | The IgniSign signature request ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "documentIds": [
        "string"
      ],
      "documents": [
        {}
      ],
      "signerIds": [
        "string"
      ],
      "signers": [
        {}
      ],
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
| `documentIds` | array<string> |  |
| `documents` | array<object> |  |
| `signerIds` | array<string> |  |
| `signers` | array<object> |  |
| `status` | string |  |

## Native endpoint

Through the native IgniSign API, this operation is `GET /v4/signature-requests/:signatureRequestId/context` (base URL `https://api.ignisign.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-signature-request-context.md) for the provider-specific parameters and requirements.

