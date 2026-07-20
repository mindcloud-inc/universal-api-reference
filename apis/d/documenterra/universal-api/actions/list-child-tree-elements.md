# Documenterra: List Child Tree Elements

Retrieves child page tree elements from Documenterra.

```
GET https://connect.mindcloud.co/v1/universal/documenterra/latest/actions/list-child-tree-elements
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documenterra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documenterra/latest/actions/list-child-tree-elements?connectionId=$CONNECTION_ID&projectId=string&tocNodeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "tocNodeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documenterra/latest/actions/list-child-tree-elements?${params}`, {
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
| `isRecursive` | boolean | no | Whether to fetch descendants recursively. |
| `projectId` | string | yes | Documenterra project identifier. |
| `tocNodeId` | string | yes | Documenterra parent tree node identifier. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Documenterra API returns.

## Native endpoint

Through the native Documenterra API, this operation is `GET /projects/:projectId/toc/nodes/:tocNodeId/children` (base URL `https://mindclouddocumenterra.try.documenterra.net/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-child-tree-elements.md) for the provider-specific parameters and requirements.

