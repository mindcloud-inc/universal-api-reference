# Dremio: Get Folder

Retrieves a folder from a Dremio project.

```
GET https://connect.mindcloud.co/v1/universal/dremio/latest/actions/get-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dremio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dremio/latest/actions/get-folder?connectionId=$CONNECTION_ID&id=string&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dremio/latest/actions/get-folder?${params}`, {
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
| `id` | string | yes |  |
| `projectId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "children": [
        {}
      ],
      "entityType": "string",
      "id": "string",
      "path": [
        "string"
      ],
      "storageUri": "string",
      "tag": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `children` | array<object> |  |
| `entityType` | string |  |
| `id` | string |  |
| `path` | array<string> |  |
| `storageUri` | string |  |
| `tag` | string |  |

## Native endpoint

Through the native Dremio API, this operation is `GET /projects/:project_id/catalog/:id` (base URL `https://api.dremio.cloud/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-folder.md) for the provider-specific parameters and requirements.

