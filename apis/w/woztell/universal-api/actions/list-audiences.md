# Woztell: List Audiences

Retrieves audiences from your Woztell workspace.

```
GET https://connect.mindcloud.co/v1/universal/woztell/latest/actions/list-audiences
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Woztell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/woztell/latest/actions/list-audiences?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/woztell/latest/actions/list-audiences?${params}`, {
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
| `variables` | object | no | Optional GraphQL variables object. Supported keys include first, after, before, audienceIds, search, and sortBy. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "apiViewer": {
          "audiences": {
            "edges": [
              {
                "node": {
                  "_id": "string",
                  "channelId": "string",
                  "createdAt": 1,
                  "description": "string",
                  "etag": "string",
                  "id": "string",
                  "name": "Ava Chen",
                  "static": true,
                  "updatedAt": 1
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
| `data.apiViewer.audiences.edges[].node._id` | string |  |
| `data.apiViewer.audiences.edges[].node.channelId` | string |  |
| `data.apiViewer.audiences.edges[].node.createdAt` | number |  |
| `data.apiViewer.audiences.edges[].node.description` | string |  |
| `data.apiViewer.audiences.edges[].node.etag` | string |  |
| `data.apiViewer.audiences.edges[].node.id` | string |  |
| `data.apiViewer.audiences.edges[].node.name` | string |  |
| `data.apiViewer.audiences.edges[].node.static` | boolean |  |
| `data.apiViewer.audiences.edges[].node.updatedAt` | number |  |
| `data.apiViewer.audiences.pageInfo.endCursor` | string |  |
| `data.apiViewer.audiences.pageInfo.hasNextPage` | boolean |  |
| `data.apiViewer.audiences.pageInfo.hasPreviousPage` | boolean |  |
| `data.apiViewer.audiences.pageInfo.startCursor` | string |  |

## Native endpoint

Through the native Woztell API, this operation is `POST /` (base URL `https://open.api.woztell.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-audiences.md) for the provider-specific parameters and requirements.

