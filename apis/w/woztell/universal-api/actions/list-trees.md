# Woztell: List Trees

Retrieves trees from your Woztell workspace.

```
GET https://connect.mindcloud.co/v1/universal/woztell/latest/actions/list-trees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Woztell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/woztell/latest/actions/list-trees?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/woztell/latest/actions/list-trees?${params}`, {
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
| `variables` | object | no | Optional GraphQL variables object. Supported keys include first, after, before, treeIds, search, and sortBy. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "apiViewer": {
          "trees": {
            "edges": [
              {
                "node": {
                  "_id": "string",
                  "appId": "string",
                  "createdAt": 1,
                  "description": "string",
                  "etag": "string",
                  "id": "string",
                  "name": "Ava Chen",
                  "system": true,
                  "type": "string",
                  "updatedAt": 1,
                  "version": 1,
                  "versionAlias": "string"
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
| `data.apiViewer.trees.edges[].node._id` | string |  |
| `data.apiViewer.trees.edges[].node.appId` | string |  |
| `data.apiViewer.trees.edges[].node.createdAt` | number |  |
| `data.apiViewer.trees.edges[].node.description` | string |  |
| `data.apiViewer.trees.edges[].node.etag` | string |  |
| `data.apiViewer.trees.edges[].node.id` | string |  |
| `data.apiViewer.trees.edges[].node.name` | string |  |
| `data.apiViewer.trees.edges[].node.system` | boolean |  |
| `data.apiViewer.trees.edges[].node.type` | string |  |
| `data.apiViewer.trees.edges[].node.updatedAt` | number |  |
| `data.apiViewer.trees.edges[].node.version` | number |  |
| `data.apiViewer.trees.edges[].node.versionAlias` | string |  |
| `data.apiViewer.trees.pageInfo.endCursor` | string |  |
| `data.apiViewer.trees.pageInfo.hasNextPage` | boolean |  |
| `data.apiViewer.trees.pageInfo.hasPreviousPage` | boolean |  |
| `data.apiViewer.trees.pageInfo.startCursor` | string |  |

## Native endpoint

Through the native Woztell API, this operation is `POST /` (base URL `https://open.api.woztell.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-trees.md) for the provider-specific parameters and requirements.

