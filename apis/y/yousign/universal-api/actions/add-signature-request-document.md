# Yousign: Add Signature Request Document

Adds a document to a Yousign signature request.

```
POST https://connect.mindcloud.co/v1/universal/yousign/latest/actions/add-signature-request-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yousign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/yousign/latest/actions/add-signature-request-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "signatureRequestId": "string",
  "file": "string",
  "nature": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/yousign/latest/actions/add-signature-request-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "signatureRequestId": "string",
    "file": "string",
    "nature": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `signatureRequestId` | string | yes | The Yousign signature request ID. |
| `file` | file | yes | Binary file to upload. |
| `nature` | string | yes | Document nature. |
| `name` | string | no | Optional document name. |
| `password` | string | no | Password for protected files, when needed. |
| `parseAnchors` | boolean | no | Automatically parse smart anchors. |
| `insertAfterId` | string | no | Insert after an existing document ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentType": "string",
      "createdAt": "string",
      "filename": "Ava Chen",
      "id": "string",
      "initials": {},
      "isLocked": true,
      "isProtected": true,
      "isSigned": true,
      "nature": "string",
      "sha256": "string",
      "totalAnchors": 1,
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentType` | string |  |
| `createdAt` | string |  |
| `filename` | string |  |
| `id` | string |  |
| `initials` | object |  |
| `isLocked` | boolean |  |
| `isProtected` | boolean |  |
| `isSigned` | boolean |  |
| `nature` | string |  |
| `sha256` | string |  |
| `totalAnchors` | number |  |
| `totalPages` | number |  |

## Native endpoint

Through the native Yousign API, this operation is `POST /signature_requests/:signatureRequestId/documents` (base URL `https://api-sandbox.yousign.app/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-signature-request-document.md) for the provider-specific parameters and requirements.

