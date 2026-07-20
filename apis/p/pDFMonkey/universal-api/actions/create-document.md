# PDFMonkey: Create Document

Creates a document asynchronously in PDFMonkey.

```
POST https://connect.mindcloud.co/v1/universal/pDFMonkey/latest/actions/create-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDFMonkey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pDFMonkey/latest/actions/create-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentTemplateId": "12345678-90ab-cdef-1234-567890abcdef"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pDFMonkey/latest/actions/create-document', {
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
| `status` | string | no | Document lifecycle state. Use pending to queue generation immediately. Default: `draft`. Example: `draft`. |
| `payload` | object | no | Data used for document generation. Example: `[object Object]`. |
| `meta` | object | no | Meta-data to attach to the document. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "document": {
        "appId": "string",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "documentTemplateId": "string",
        "downloadUrl": "https://example.com",
        "failureCause": "string",
        "filename": "Ava Chen",
        "generationLogs": [
          {}
        ],
        "id": "string",
        "meta": "string",
        "outputType": "string",
        "payload": "string",
        "previewUrl": "https://example.com",
        "publicShareLink": "https://example.com",
        "status": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z",
        "xmlData": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `document.appId` | string | Owning PDFMonkey app ID. |
| `document.createdAt` | date | Creation timestamp. |
| `document.documentTemplateId` | string | Source template ID. |
| `document.downloadUrl` | string | Download URL. |
| `document.failureCause` | string | Failure cause when generation does not succeed. |
| `document.filename` | string | Generated file name. |
| `document.generationLogs` | array<object> | Generation log entries. |
| `document.id` | string | Document ID. |
| `document.meta` | string | Serialized document metadata. |
| `document.outputType` | string | Generated file output type. |
| `document.payload` | string | Serialized document payload. |
| `document.previewUrl` | string | Preview URL. |
| `document.publicShareLink` | string | Public share URL. |
| `document.status` | string | Document lifecycle status. |
| `document.updatedAt` | date | Last update timestamp. |
| `document.xmlData` | string | Serialized XML data when present. |

## Native endpoint

Through the native PDFMonkey API, this operation is `POST /documents` (base URL `https://api.pdfmonkey.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-document.md) for the provider-specific parameters and requirements.

