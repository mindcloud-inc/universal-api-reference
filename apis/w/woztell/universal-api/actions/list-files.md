# Woztell: List Files

Retrieves files from your Woztell workspace.

```
GET https://connect.mindcloud.co/v1/universal/woztell/latest/actions/list-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Woztell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/woztell/latest/actions/list-files?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/woztell/latest/actions/list-files?${params}`, {
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
| `variables` | object | no | Optional GraphQL variables object. Supported keys include additionalIds, after, appId, before, fileIds, fileType, first, from, hideApiFiles, last, search, sizeMax, sizeMin, sortBy, and to. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "apiViewer": {
          "files": {
            "edges": [
              {
                "node": {
                  "_id": "string",
                  "createdAt": 1,
                  "error": "string",
                  "etag": "string",
                  "fileName": "Ava Chen",
                  "fileType": "string",
                  "id": "string",
                  "size": 1,
                  "updatedAt": 1,
                  "url": "https://example.com"
                }
              }
            ],
            "pageInfo": {
              "endCursor": "string",
              "hasNextPage": true,
              "hasPreviousPage": true,
              "startCursor": "string"
            }
          }
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.apiViewer.files.edges[].node._id` | string |  |
| `data.apiViewer.files.edges[].node.createdAt` | number |  |
| `data.apiViewer.files.edges[].node.error` | string |  |
| `data.apiViewer.files.edges[].node.etag` | string |  |
| `data.apiViewer.files.edges[].node.fileName` | string |  |
| `data.apiViewer.files.edges[].node.fileType` | string |  |
| `data.apiViewer.files.edges[].node.id` | string |  |
| `data.apiViewer.files.edges[].node.size` | number |  |
| `data.apiViewer.files.edges[].node.updatedAt` | number |  |
| `data.apiViewer.files.edges[].node.url` | string |  |
| `data.apiViewer.files.pageInfo.endCursor` | string |  |
| `data.apiViewer.files.pageInfo.hasNextPage` | boolean |  |
| `data.apiViewer.files.pageInfo.hasPreviousPage` | boolean |  |
| `data.apiViewer.files.pageInfo.startCursor` | string |  |

## Native endpoint

Through the native Woztell API, this operation is `POST /` (base URL `https://open.api.woztell.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-files.md) for the provider-specific parameters and requirements.

