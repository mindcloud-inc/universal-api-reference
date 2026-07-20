# RightSignature: Get Archived Document By Original GUID

Retrieves an archived RightSignature document by original GUID.

```
GET https://connect.mindcloud.co/v1/universal/rightSignature/latest/actions/get-archived-document-by-original-guid
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RightSignature `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rightSignature/latest/actions/get-archived-document-by-original-guid?connectionId=$CONNECTION_ID&originalGuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "originalGuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rightSignature/latest/actions/get-archived-document-by-original-guid?${params}`, {
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
| `originalGuid` | string | yes | Archived Document Original GUID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "audits": [
        {}
      ],
      "ccParties": [
        "string"
      ],
      "documentExecutedAt": "2026-05-07T12:00:00.000Z",
      "documentExpiresAt": "2026-05-07T12:00:00.000Z",
      "documentSentAt": "2026-05-07T12:00:00.000Z",
      "documentState": "string",
      "fileAttachments": [
        "string"
      ],
      "id": "string",
      "imageHeight": 1,
      "imageWidth": 1,
      "name": "Ava Chen",
      "originalGuid": "string",
      "pageImages": [
        {}
      ],
      "senderEmail": "ava@example.com",
      "sharedWith": [
        "string"
      ],
      "signedPdfUrl": "https://example.com",
      "signers": [
        {}
      ],
      "tags": {},
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `audits` | array<object> |  |
| `ccParties` | array<string> |  |
| `documentExecutedAt` | date |  |
| `documentExpiresAt` | date |  |
| `documentSentAt` | date |  |
| `documentState` | string |  |
| `fileAttachments` | array<string> |  |
| `id` | string |  |
| `imageHeight` | number |  |
| `imageWidth` | number |  |
| `name` | string |  |
| `originalGuid` | string |  |
| `pageImages` | array<object> |  |
| `senderEmail` | string |  |
| `sharedWith` | array<string> |  |
| `signedPdfUrl` | string |  |
| `signers` | array<object> |  |
| `tags` | object |  |
| `userId` | string |  |

## Native endpoint

Through the native RightSignature API, this operation is `GET /archived_documents_by_original_guid/:original_guid` (base URL `https://api.rightsignature.com/public/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-archived-document-by-original-guid.md) for the provider-specific parameters and requirements.

