# Pdfless: Generate PDF



```
POST https://connect.mindcloud.co/v1/universal/pdfless/latest/actions/generate-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pdfless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pdfless/latest/actions/generate-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pdfless/latest/actions/generate-pdf', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateId` | string | yes | Unique identifier of the template used to generate the PDF. |
| `referenceId` | string | no | Identifier that matches a reference in the caller system. |
| `payload` | object | no | Data in JSON format. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `encryptionUserPassword` | string | no | Password required to open the generated document. |
| `encryptionOwnerPassword` | string | no | Permission password used to restrict document functionality. |
| `encryptionAllowPrinting` | boolean | no | Allow users to print the document. |
| `encryptionAllowModifying` | boolean | no | Allow users to modify the document. |
| `encryptionAllowModifyAnnotations` | boolean | no | Allow users to modify document annotations. |
| `encryptionAllowContentCopying` | boolean | no | Allow users to copy document content. |
| `encryptionAllowScreenreaders` | boolean | no | Allow screenreaders to access document content. |
| `encryptionAllowFormFilling` | boolean | no | Allow users to fill document forms. |
| `encryptionAllowDocumentAssembly` | boolean | no | Allow cross-document assembly operations. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "downloadUrl": "https://example.com",
      "expires": "2026-05-07T12:00:00.000Z",
      "referenceId": "string",
      "templateId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Timestamp when the PDF was created. |
| `downloadUrl` | string | Temporary URL of the generated PDF. |
| `expires` | date | Timestamp when the download URL expires. |
| `referenceId` | string | Reference identifier supplied in the request. |
| `templateId` | string | Unique identifier of the template used to generate the PDF. |

## Native endpoint

Through the native Pdfless API, this operation is `POST /v1/pdfs` (base URL `https://api.pdfless.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-pdf.md) for the provider-specific parameters and requirements.

