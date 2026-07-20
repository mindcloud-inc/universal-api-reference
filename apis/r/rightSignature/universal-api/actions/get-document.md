# RightSignature: Get Document

Retrieves a specific document from RightSignature.

```
GET https://connect.mindcloud.co/v1/universal/rightSignature/latest/actions/get-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RightSignature `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rightSignature/latest/actions/get-document?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rightSignature/latest/actions/get-document?${params}`, {
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
| `id` | string | yes | Document ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "audits": [
        "string"
      ],
      "currentSignerId": "string",
      "embedCodes": "string",
      "executedAt": "string",
      "expiredAt": "2026-05-07T12:00:00.000Z",
      "filename": "Ava Chen",
      "formFields": [
        {}
      ],
      "id": "string",
      "identityMethod": "string",
      "inPerson": true,
      "kba": true,
      "mergedDocumentCertificateUrl": "https://example.com",
      "mergeFieldValues": [
        "string"
      ],
      "name": "Ava Chen",
      "originalFileUrl": "https://example.com",
      "pageImageUrls": [
        "https://example.com"
      ],
      "passcodePinEnabled": true,
      "recipients": [
        {}
      ],
      "sender": {},
      "sentAt": "2026-05-07T12:00:00.000Z",
      "sharedWith": [
        "string"
      ],
      "signatureCertificateUrl": "https://example.com",
      "signedPdfUrl": "https://example.com",
      "state": "string",
      "tags": {},
      "thumbnailUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `audits` | array<string> |  |
| `currentSignerId` | string |  |
| `embedCodes` | string |  |
| `executedAt` | string |  |
| `expiredAt` | date |  |
| `filename` | string |  |
| `formFields` | array<object> |  |
| `id` | string |  |
| `identityMethod` | string |  |
| `inPerson` | boolean |  |
| `kba` | boolean |  |
| `mergedDocumentCertificateUrl` | string |  |
| `mergeFieldValues` | array<string> |  |
| `name` | string |  |
| `originalFileUrl` | string |  |
| `pageImageUrls` | array<string> |  |
| `passcodePinEnabled` | boolean |  |
| `recipients` | array<object> |  |
| `sender` | object |  |
| `sentAt` | date |  |
| `sharedWith` | array<string> |  |
| `signatureCertificateUrl` | string |  |
| `signedPdfUrl` | string |  |
| `state` | string |  |
| `tags` | object |  |
| `thumbnailUrl` | string |  |

## Native endpoint

Through the native RightSignature API, this operation is `GET /documents/:id` (base URL `https://api.rightsignature.com/public/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document.md) for the provider-specific parameters and requirements.

