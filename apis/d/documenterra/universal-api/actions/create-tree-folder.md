# Documenterra: Create Tree Folder

Creates a page tree folder in Documenterra.

```
POST https://connect.mindcloud.co/v1/universal/documenterra/latest/actions/create-tree-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documenterra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/documenterra/latest/actions/create-tree-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "caption": "string",
  "projectId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/documenterra/latest/actions/create-tree-folder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "caption": "string",
    "projectId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `caption` | string | yes | Tree folder caption. |
| `isShowInToc` | boolean | no | Whether to show the folder in the tree of contents. |
| `ordinalNo` | number | no | Optional folder order index. |
| `parentId` | string | no | Optional parent tree node identifier. |
| `projectId` | string | yes | Documenterra project identifier. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Documenterra API returns.

## Native endpoint

Through the native Documenterra API, this operation is `POST /projects/:projectId/toc/nodes` (base URL `https://mindclouddocumenterra.try.documenterra.net/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-tree-folder.md) for the provider-specific parameters and requirements.

