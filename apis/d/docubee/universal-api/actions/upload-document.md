# Docubee: Upload Document

Uploads a new document to Docubee.

```
POST https://connect.mindcloud.co/v1/universal/docubee/latest/actions/upload-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docubee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docubee/latest/actions/upload-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docubee/latest/actions/upload-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contentType` | string | no | The MIME type of the uploaded document. Defaults to application/pdf. |
| `fileContentBase64` | string | no | The document file content encoded as base64. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdOn": "2026-05-07T12:00:00.000Z",
      "documentId": "string",
      "name": "Ava Chen",
      "status": "string",
      "tenantId": "string",
      "updatedOn": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdOn` | date | Creation timestamp when returned by Docubee. |
| `documentId` | string | Created document identifier. |
| `name` | string | Document name when returned by Docubee. |
| `status` | string | Document status when returned by Docubee. |
| `tenantId` | string | Owning Docubee tenant identifier when returned by Docubee. |
| `updatedOn` | date | Last update timestamp when returned by Docubee. |

## Native endpoint

Through the native Docubee API, this operation is `POST /documents` (base URL `https://docubee.app/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-document.md) for the provider-specific parameters and requirements.

