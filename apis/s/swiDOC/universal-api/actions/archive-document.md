# swiDOC: Archive Document

Archives a document in swiDOC.

```
POST https://connect.mindcloud.co/v1/universal/swiDOC/latest/actions/archive-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a swiDOC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/swiDOC/latest/actions/archive-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileContent": "string",
  "metadata.fileName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/swiDOC/latest/actions/archive-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileContent": "string",
    "metadata.fileName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileContent` | string | yes | Base64 encoded file content. |
| `metadata.fileName` | string | yes | Name of the file including extension. |
| `metadata.filePath` | string | no | Optional archive folder path. The folder will be created if it does not exist. |
| `metadata.description` | string | no | Optional text used for indexing the document. |
| `metadata.tags[]` | array<string> | no | Optional tags for the document. Accepts multiple values as an array. |
| `metadata.archiveDuration` | number | no | Optional archiving duration in milliseconds; empty archives forever. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `metadata.searchAttributes[]` | array<object> | no | Optional array of search attribute objects. |

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
| `documentId` | string | ID of the archived document. |
| `success` | boolean | Whether the archive request was accepted for processing. |

## Native endpoint

Through the native swiDOC API, this operation is `POST /documents` (base URL `https://app.swidoc.ch/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/archive-document.md) for the provider-specific parameters and requirements.

