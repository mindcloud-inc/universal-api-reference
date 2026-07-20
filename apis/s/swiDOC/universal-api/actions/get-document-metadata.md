# swiDOC: Get Document Metadata

Retrieves document metadata from swiDOC by document ID.

```
GET https://connect.mindcloud.co/v1/universal/swiDOC/latest/actions/get-document-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a swiDOC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/swiDOC/latest/actions/get-document-metadata?connectionId=$CONNECTION_ID&documentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/swiDOC/latest/actions/get-document-metadata?${params}`, {
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
| `documentId` | string | yes | Unique ID of the document whose metadata should be retrieved. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "metadata": {
        "archivingEndDate": 1,
        "createdAt": 1,
        "description": "string",
        "fileName": "Ava Chen",
        "filePath": "string",
        "searchAttributes": [
          {}
        ],
        "tags": [
          "string"
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `metadata` | object | Document metadata object. |
| `metadata.archivingEndDate` | number | Unix timestamp in milliseconds when archiving ends; 0 means endless. |
| `metadata.createdAt` | number | Unix timestamp in milliseconds when the file was archived. |
| `metadata.description` | string | Document description. |
| `metadata.fileName` | string | Document file name. |
| `metadata.filePath` | string | Document folder path. |
| `metadata.searchAttributes` | array<object> | Search attribute objects. |
| `metadata.tags` | array<string> | Document tags. |

## Native endpoint

Through the native swiDOC API, this operation is `GET /documents/:documentId/metadata` (base URL `https://app.swidoc.ch/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document-metadata.md) for the provider-specific parameters and requirements.

