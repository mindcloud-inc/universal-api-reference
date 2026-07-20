# PDFMonkey: Generate Document Synchronously

Generates a document synchronously in PDFMonkey.

```
POST https://connect.mindcloud.co/v1/universal/pDFMonkey/latest/actions/generate-document-synchronously
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDFMonkey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pDFMonkey/latest/actions/generate-document-synchronously" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentTemplateId": "12345678-90ab-cdef-1234-567890abcdef"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pDFMonkey/latest/actions/generate-document-synchronously', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentTemplateId": "12345678-90ab-cdef-1234-567890abcdef"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentTemplateId` | string | yes | ID of the source Template to use. Example: `12345678-90ab-cdef-1234-567890abcdef`. |
| `payload` | object | no | Data to use for the Document generation. Example: `[object Object]`. |
| `meta` | object | no | Meta-data to attach to the Document. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "documentCard": {
        "appId": "string",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "documentTemplateId": "string",
        "documentTemplateIdentifier": "string",
        "downloadUrl": "https://example.com",
        "failureCause": "string",
        "filename": "Ava Chen",
        "id": "string",
        "meta": "string",
        "outputType": "string",
        "previewUrl": "https://example.com",
        "publicShareLink": "https://example.com",
        "status": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `documentCard.appId` | string | Owning PDFMonkey app ID. |
| `documentCard.createdAt` | date | Creation timestamp. |
| `documentCard.documentTemplateId` | string | Source template ID. |
| `documentCard.documentTemplateIdentifier` | string | Source template identifier. |
| `documentCard.downloadUrl` | string | Download URL. |
| `documentCard.failureCause` | string | Failure cause when generation does not succeed. |
| `documentCard.filename` | string | Generated file name. |
| `documentCard.id` | string | Document card ID. |
| `documentCard.meta` | string | Serialized document metadata. |
| `documentCard.outputType` | string | Generated file output type. |
| `documentCard.previewUrl` | string | Preview URL. |
| `documentCard.publicShareLink` | string | Public share URL. |
| `documentCard.status` | string | Generation status. |
| `documentCard.updatedAt` | date | Last update timestamp. |

## Native endpoint

Through the native PDFMonkey API, this operation is `POST /documents/sync` (base URL `https://api.pdfmonkey.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-document-synchronously.md) for the provider-specific parameters and requirements.

