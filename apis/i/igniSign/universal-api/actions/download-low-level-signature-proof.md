# IgniSign: Download Low-Level Signature Proof



```
GET https://connect.mindcloud.co/v1/universal/igniSign/latest/actions/download-low-level-signature-proof
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IgniSign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/igniSign/latest/actions/download-low-level-signature-proof?connectionId=$CONNECTION_ID&documentId=string&signatureType=string&signerId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "string",
  "signatureType": "string",
  "signerId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/igniSign/latest/actions/download-low-level-signature-proof?${params}`, {
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
| `documentId` | string | yes | The IgniSign document ID. |
| `signatureType` | string | yes | The signature type to download. |
| `signerId` | string | yes | The IgniSign signer ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "data": {},
      "message": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `data` | object |  |
| `message` | string |  |
| `name` | string |  |

## Native endpoint

Through the native IgniSign API, this operation is `GET /v4/documents/:documentId/signatures/:signatureType/signers/:signerId` (base URL `https://api.ignisign.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-low-level-signature-proof.md) for the provider-specific parameters and requirements.

