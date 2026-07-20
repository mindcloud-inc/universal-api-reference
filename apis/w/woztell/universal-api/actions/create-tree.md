# Woztell: Create Tree

Creates a tree in your Woztell workspace.

```
POST https://connect.mindcloud.co/v1/universal/woztell/latest/actions/create-tree
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Woztell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/woztell/latest/actions/create-tree" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variables.input.name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/woztell/latest/actions/create-tree', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variables.input.name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables.input.name` | string | yes |  |
| `variables.input.description` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "createTree": {
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
| `data.createTree.clientMutationId` | string |  |
| `data.createTree.tree._id` | string |  |
| `data.createTree.tree.appId` | string |  |
| `data.createTree.tree.createdAt` | number |  |
| `data.createTree.tree.description` | string |  |
| `data.createTree.tree.etag` | string |  |
| `data.createTree.tree.id` | string |  |
| `data.createTree.tree.name` | string |  |
| `data.createTree.tree.system` | boolean |  |
| `data.createTree.tree.type` | string |  |
| `data.createTree.tree.updatedAt` | number |  |
| `data.createTree.tree.version` | number |  |
| `data.createTree.tree.versionAlias` | string |  |

## Native endpoint

Through the native Woztell API, this operation is `POST /` (base URL `https://open.api.woztell.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-tree.md) for the provider-specific parameters and requirements.

