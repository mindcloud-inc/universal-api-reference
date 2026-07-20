# Figma: Get File Nodes

Retrieves nodes from a Figma file by ID.

```
GET https://connect.mindcloud.co/v1/universal/figma/latest/actions/get-file-nodes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Figma `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/figma/latest/actions/get-file-nodes?connectionId=$CONNECTION_ID&key=string&ids=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "key": "string",
  "ids": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/figma/latest/actions/get-file-nodes?${params}`, {
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
| `key` | string | yes | Key of the file to read nodes from. |
| `ids` | string | yes | Comma-separated node IDs to fetch. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `version` | string | no | Version ID to fetch nodes from. |
| `depth` | number | no | Maximum depth of node traversal. |
| `geometry` | string | no | Geometry payload mode to include in response. |
| `pluginData` | string | no | Comma-separated plugin IDs to include plugin data for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "editorType": "string",
      "lastModified": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "nodes": {},
      "role": "string",
      "thumbnailUrl": "https://example.com",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `editorType` | string |  |
| `lastModified` | date |  |
| `name` | string |  |
| `nodes` | object |  |
| `role` | string |  |
| `thumbnailUrl` | string |  |
| `version` | string |  |

## Native endpoint

Through the native Figma API, this operation is `GET /files/:key/nodes` (base URL `https://api.figma.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-file-nodes.md) for the provider-specific parameters and requirements.

