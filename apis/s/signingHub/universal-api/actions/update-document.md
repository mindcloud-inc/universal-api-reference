# SigningHub: Update Document

Updates a document in SigningHub.

```
PUT https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/update-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SigningHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/update-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "packageId": "11191608",
  "documentId": "13459159",
  "file": "Raw binary PDF content"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/update-document', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "packageId": "11191608",
    "documentId": "13459159",
    "file": "Raw binary PDF content"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `packageId` | number | yes | The document package containing the document to replace. Example: `11191608`. |
| `documentId` | number | yes | The document to replace. Example: `13459159`. |
| `file` | string | yes | The replacement raw binary document content. Example: `Raw binary PDF content`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "certify": {},
      "document_height": 1,
      "document_id": 1,
      "document_name": "Ava Chen",
      "document_order": 1,
      "document_pages": 1,
      "document_size": 1,
      "document_source": "string",
      "document_type": "string",
      "document_width": 1,
      "lock_form_fields": true,
      "metadata": {},
      "modified_on": "string",
      "package_name": "Ava Chen",
      "uploaded_on": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `certify` | object |  |
| `document_height` | number |  |
| `document_id` | number |  |
| `document_name` | string |  |
| `document_order` | number |  |
| `document_pages` | number |  |
| `document_size` | number |  |
| `document_source` | string |  |
| `document_type` | string |  |
| `document_width` | number |  |
| `lock_form_fields` | boolean |  |
| `metadata` | object |  |
| `modified_on` | string |  |
| `package_name` | string |  |
| `uploaded_on` | string |  |

## Native endpoint

Through the native SigningHub API, this operation is `PUT /v4/packages/:packageId/documents/:documentId/update` (base URL `https://api.signinghub.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-document.md) for the provider-specific parameters and requirements.

