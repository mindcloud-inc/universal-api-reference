# Woztell: Get Tree

Retrieves a tree from your Woztell workspace.

```
GET https://connect.mindcloud.co/v1/universal/woztell/latest/actions/get-tree
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Woztell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/woztell/latest/actions/get-tree?connectionId=$CONNECTION_ID&variables.treeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variables.treeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/woztell/latest/actions/get-tree?${params}`, {
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
| `variables.treeId` | string | yes | Tree id in Stella. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "apiViewer": {
          "tree": {
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
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.apiViewer.tree._id` | string |  |
| `data.apiViewer.tree.appId` | string |  |
| `data.apiViewer.tree.createdAt` | number |  |
| `data.apiViewer.tree.description` | string |  |
| `data.apiViewer.tree.etag` | string |  |
| `data.apiViewer.tree.id` | string |  |
| `data.apiViewer.tree.name` | string |  |
| `data.apiViewer.tree.system` | boolean |  |
| `data.apiViewer.tree.type` | string |  |
| `data.apiViewer.tree.updatedAt` | number |  |
| `data.apiViewer.tree.version` | number |  |
| `data.apiViewer.tree.versionAlias` | string |  |

## Native endpoint

Through the native Woztell API, this operation is `POST /` (base URL `https://open.api.woztell.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tree.md) for the provider-specific parameters and requirements.

