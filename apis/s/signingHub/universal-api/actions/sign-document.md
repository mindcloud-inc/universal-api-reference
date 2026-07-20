# SigningHub: Sign Document

Signs a document in SigningHub.

```
POST https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/sign-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SigningHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/sign-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "packageId": 1,
  "documentId": 1,
  "fieldName": "SH_SIGNATURE_123456",
  "handSignatureImage": "Base64 PNG or JPG signature image"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/sign-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "packageId": 1,
    "documentId": 1,
    "fieldName": "SH_SIGNATURE_123456",
    "handSignatureImage": "Base64 PNG or JPG signature image"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `packageId` | number | yes | The document package containing the document to sign. |
| `documentId` | number | yes | The document to sign. |
| `fieldName` | string | yes | The signature field name to sign. This field is required by the SigningHub API. Example: `SH_SIGNATURE_123456`. |
| `handSignatureImage` | string | yes | Base64-encoded hand signature image to apply when signing. Example: `Base64 PNG or JPG signature image`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authentication_access_token": "string",
      "field_name": "Ava Chen",
      "status": "string",
      "transaction_id": "string",
      "verification": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authentication_access_token` | string |  |
| `field_name` | string |  |
| `status` | string |  |
| `transaction_id` | string |  |
| `verification` | object |  |

## Native endpoint

Through the native SigningHub API, this operation is `POST /v4/packages/:packageId/documents/:documentId/sign` (base URL `https://api.signinghub.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/sign-document.md) for the provider-specific parameters and requirements.

