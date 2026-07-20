# Yousign: List Signature Request Documents

Retrieves documents from a Yousign signature request.

```
GET https://connect.mindcloud.co/v1/universal/yousign/latest/actions/list-signature-request-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yousign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yousign/latest/actions/list-signature-request-documents?connectionId=$CONNECTION_ID&signatureRequestId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "signatureRequestId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yousign/latest/actions/list-signature-request-documents?${params}`, {
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
| `signatureRequestId` | string | yes | The Yousign signature request ID. |
| `natureEq` | string | no | Filter documents by nature. |

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

Through the native Yousign API, this operation is `GET /signature_requests/:signatureRequestId/documents` (base URL `https://api-sandbox.yousign.app/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-signature-request-documents.md) for the provider-specific parameters and requirements.

