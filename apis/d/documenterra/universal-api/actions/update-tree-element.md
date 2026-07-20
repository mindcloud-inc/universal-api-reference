# Documenterra: Update Tree Element

Updates an existing page tree element in Documenterra.

```
PUT https://connect.mindcloud.co/v1/universal/documenterra/latest/actions/update-tree-element
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documenterra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/documenterra/latest/actions/update-tree-element" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "caption": "string",
  "projectId": "string",
  "tocNodeId": "string",
  "updatedFields": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/documenterra/latest/actions/update-tree-element', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "caption": "string",
    "projectId": "string",
    "tocNodeId": "string",
    "updatedFields": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `caption` | string | yes | Updated tree node caption. |
| `isShowInToc` | boolean | no | Whether to show the node in the tree of contents. |
| `ordinalNo` | number | no | Updated node order index. |
| `parentId` | string | no | Updated parent tree node identifier. |
| `projectId` | string | yes | Documenterra project identifier. |
| `tocNodeId` | string | yes | Documenterra tree node identifier. |
| `updatedFields` | string | yes | Comma-separated list of tree fields to update. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Documenterra API returns.

## Native endpoint

Through the native Documenterra API, this operation is `PATCH /projects/:projectId/toc/nodes/:tocNodeId` (base URL `https://mindclouddocumenterra.try.documenterra.net/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-tree-element.md) for the provider-specific parameters and requirements.

