# swiDOC: Update Document Metadata

Updates document metadata in swiDOC by document ID.

```
PUT https://connect.mindcloud.co/v1/universal/swiDOC/latest/actions/update-document-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a swiDOC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/swiDOC/latest/actions/update-document-metadata" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/swiDOC/latest/actions/update-document-metadata', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentId` | string | yes | Unique ID of the document whose metadata should be updated. |
| `fileName` | string | no | Optional new file name including extension. |
| `filePath` | string | no | Optional new folder path. |
| `description` | string | no | Optional document description. |
| `tags[]` | array<string> | no | Optional replacement tag delta for the document. Accepts multiple values as an array. |
| `archiveDuration` | number | no | Optional milliseconds by which the archiving duration should be extended. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `searchAttributes[]` | array<object> | no | Optional array of search attribute objects. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "documentId": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `documentId` | string | ID of the updated document. |
| `success` | boolean | Whether the metadata update was processed successfully. |

## Native endpoint

Through the native swiDOC API, this operation is `PATCH /documents/:documentId/metadata` (base URL `https://app.swidoc.ch/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-document-metadata.md) for the provider-specific parameters and requirements.

