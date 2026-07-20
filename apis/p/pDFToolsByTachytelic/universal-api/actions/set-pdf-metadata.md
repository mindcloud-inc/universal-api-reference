# PDF Tools by Tachytelic: Set PDF Metadata



```
GET https://connect.mindcloud.co/v1/universal/pDFToolsByTachytelic/latest/actions/set-pdf-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDF Tools by Tachytelic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pDFToolsByTachytelic/latest/actions/set-pdf-metadata?connectionId=$CONNECTION_ID&pdfFileContent=Base64%20PDF%20content" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pdfFileContent": "Base64 PDF content"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pDFToolsByTachytelic/latest/actions/set-pdf-metadata?${params}`, {
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
| `pdfFileContent` | string | yes | Base64-encoded PDF content. Example: `Base64 PDF content`. |
| `title` | string | no | Document title metadata to set. Example: `Document title`. |
| `author` | string | no | Document author metadata to set. Example: `Document author`. |
| `subject` | string | no | Document subject metadata to set. Example: `Document subject`. |
| `keywords` | string | no | Document keywords metadata to set. Example: `Comma-separated keywords`. |
| `creationDate` | string | no | Document creation date metadata to set. Example: `2026-05-01`. |
| `modificationDate` | string | no | Document modification date metadata to set. Example: `2026-05-01`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "UpdatedPdf": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `UpdatedPdf` | string | Base64-encoded PDF with updated metadata. |

## Native endpoint

Through the native PDF Tools by Tachytelic API, this operation is `POST /setmetadata` (base URL `https://pdf.tachytelic.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-pdf-metadata.md) for the provider-specific parameters and requirements.

