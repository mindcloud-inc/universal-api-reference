# SigningHub: Upload Document Base64

Uploads a base64 document to SigningHub.

```
POST https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/upload-document-base64
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SigningHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/upload-document-base64" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "packageId": "11191528",
  "document": "Base64 PDF content"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/upload-document-base64', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "packageId": "11191528",
    "document": "Base64 PDF content"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `packageId` | number | yes | Package ID of the package to which the document is being added. Example: `11191528`. |
| `document` | string | yes | Base64-encoded document content. Example: `Base64 PDF content`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "document_id": 1,
      "document_name": "Ava Chen",
      "document_pages": 1,
      "document_type": "string",
      "package_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `document_id` | number |  |
| `document_name` | string |  |
| `document_pages` | number |  |
| `document_type` | string |  |
| `package_name` | string |  |

## Native endpoint

Through the native SigningHub API, this operation is `POST /v4/packages/:packageId/documents/base64` (base URL `https://api.signinghub.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-document-base64.md) for the provider-specific parameters and requirements.

