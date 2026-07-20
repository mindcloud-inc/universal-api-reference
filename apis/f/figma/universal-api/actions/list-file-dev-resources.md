# Figma: List File Dev Resources

Retrieves dev resources from a Figma file.

```
GET https://connect.mindcloud.co/v1/universal/figma/latest/actions/list-file-dev-resources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Figma `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/figma/latest/actions/list-file-dev-resources?connectionId=$CONNECTION_ID&file_key=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "file_key": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/figma/latest/actions/list-file-dev-resources?${params}`, {
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
| `file_key` | string | yes | Main Figma file key (not a branch key). |
| `node_ids` | string | no | Comma-separated node IDs to scope returned dev resources. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fileKey": "string",
      "id": "string",
      "name": "Ava Chen",
      "nodeId": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fileKey` | string |  |
| `id` | string |  |
| `name` | string |  |
| `nodeId` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Figma API, this operation is `GET https://api.figma.com/v1/files/:file_key/dev_resources` (base URL `https://api.figma.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-file-dev-resources.md) for the provider-specific parameters and requirements.

