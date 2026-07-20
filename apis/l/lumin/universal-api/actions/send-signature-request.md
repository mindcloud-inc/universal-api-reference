# Lumin: Send Signature Request



```
POST https://connect.mindcloud.co/v1/universal/lumin/latest/actions/send-signature-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lumin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lumin/latest/actions/send-signature-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileUrl": "https://example.com",
  "title": "string",
  "signers[]": [
    {}
  ],
  "expiresAt": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lumin/latest/actions/send-signature-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileUrl": "https://example.com",
    "title": "string",
    "signers[]": [{}],
    "expiresAt": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileUrl` | string | yes | URL of the file to download and send for signature. |
| `title` | string | yes | Title of the signature request. |
| `signers[]` | array<object> | yes | Array of signer objects with email_address and name, plus group when using ORDER signing. |
| `expiresAt` | number | yes | Future Unix timestamp in milliseconds when the request expires. |
| `signingType` | string | no | Signing order. SAME_TIME or ORDER. Default: `SAME_TIME`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "signatureRequest": {
        "createdAt": 1,
        "signatureRequestId": "string",
        "status": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `signatureRequest.createdAt` | number |  |
| `signatureRequest.signatureRequestId` | string |  |
| `signatureRequest.status` | string |  |

## Native endpoint

Through the native Lumin API, this operation is `POST /signature_request/send` (base URL `https://api.luminpdf.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-signature-request.md) for the provider-specific parameters and requirements.

