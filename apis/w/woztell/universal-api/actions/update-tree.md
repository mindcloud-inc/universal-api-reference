# Woztell: Update Tree

Updates a tree in your Woztell workspace.

```
PUT https://connect.mindcloud.co/v1/universal/woztell/latest/actions/update-tree
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Woztell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/woztell/latest/actions/update-tree" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variables.input.treeId": "string",
  "variables.input.etag": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/woztell/latest/actions/update-tree', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variables.input.treeId": "string",
    "variables.input.etag": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables.input.treeId` | string | yes | Raw Woztell tree _id to update. |
| `variables.input.etag` | string | yes | Current Woztell tree etag for optimistic concurrency. |
| `variables.input.description` | string | no | Updated tree description. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "updateTree": {
          "clientMutationId": "string",
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
| `data.updateTree.clientMutationId` | string |  |
| `data.updateTree.tree._id` | string |  |
| `data.updateTree.tree.appId` | string |  |
| `data.updateTree.tree.createdAt` | number |  |
| `data.updateTree.tree.description` | string |  |
| `data.updateTree.tree.etag` | string |  |
| `data.updateTree.tree.id` | string |  |
| `data.updateTree.tree.name` | string |  |
| `data.updateTree.tree.system` | boolean |  |
| `data.updateTree.tree.type` | string |  |
| `data.updateTree.tree.updatedAt` | number |  |
| `data.updateTree.tree.version` | number |  |
| `data.updateTree.tree.versionAlias` | string |  |

## Native endpoint

Through the native Woztell API, this operation is `POST /` (base URL `https://open.api.woztell.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-tree.md) for the provider-specific parameters and requirements.

