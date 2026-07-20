# Figma: Get File

Retrieves a Figma file by key.

```
GET https://connect.mindcloud.co/v1/universal/figma/latest/actions/get-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Figma `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/figma/latest/actions/get-file?connectionId=$CONNECTION_ID&key=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "key": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/figma/latest/actions/get-file?${params}`, {
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
| `key` | string | yes | Key of the file to retrieve. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `version` | string | no | Version ID to retrieve a specific historical file snapshot. |
| `ids` | string | no | Comma-separated node IDs to return only selected nodes. |
| `depth` | number | no | Maximum depth of node traversal to return. |
| `geometry` | string | no | Geometry payload mode to include in response. |
| `pluginData` | string | no | Comma-separated plugin IDs to include plugin data for. |
| `branchData` | boolean | no | Whether to include branch metadata in response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "branches": [
        {}
      ],
      "components": {},
      "componentSets": {},
      "document": {},
      "editorType": "string",
      "lastModified": "2026-05-07T12:00:00.000Z",
      "linkAccess": "https://example.com",
      "mainFileKey": "string",
      "name": "Ava Chen",
      "role": "string",
      "schemaVersion": 1,
      "styles": {},
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
| `branches` | array<object> |  |
| `components` | object |  |
| `componentSets` | object |  |
| `document` | object |  |
| `editorType` | string |  |
| `lastModified` | date |  |
| `linkAccess` | string |  |
| `mainFileKey` | string |  |
| `name` | string |  |
| `role` | string |  |
| `schemaVersion` | number |  |
| `styles` | object |  |
| `thumbnailUrl` | string |  |
| `version` | string |  |

## Native endpoint

Through the native Figma API, this operation is `GET /files/:key` (base URL `https://api.figma.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-file.md) for the provider-specific parameters and requirements.

