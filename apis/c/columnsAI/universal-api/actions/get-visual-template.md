# Columns AI: Get Visual Template

Retrieves a visual template from Columns AI by visual ID.

```
GET https://connect.mindcloud.co/v1/universal/columnsAI/latest/actions/get-visual-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Columns AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/columnsAI/latest/actions/get-visual-template?connectionId=$CONNECTION_ID&id=U6tALuJ3cTdPFw" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "U6tALuJ3cTdPFw"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/columnsAI/latest/actions/get-visual-template?${params}`, {
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
| `id` | string | yes | Columns visual ID to load as a template. Example: `U6tALuJ3cTdPFw`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "access": {},
      "createdAt": {},
      "creator": "string",
      "current": "string",
      "graph": "string",
      "id": "string",
      "key": "string",
      "name": "Ava Chen",
      "shared": true,
      "thumb_base64": "string",
      "updatedAt": {},
      "version": 1,
      "versions": 1,
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access` | object | Access settings for the visual. |
| `createdAt` | object | Created timestamp object from Columns. |
| `creator` | string | Creator user ID. |
| `current` | string | Current version identifier. |
| `graph` | string | Compressed graph payload returned by the Columns snapshot endpoint. |
| `id` | string | Columns visual ID. |
| `key` | string | CDN key for the visual thumbnail or asset. |
| `name` | string | Visual name. |
| `shared` | boolean | Whether the visual is shared. |
| `thumb_base64` | string | Thumbnail URL returned by Columns. |
| `updatedAt` | object | Updated timestamp object from Columns. |
| `version` | number | Current visual schema version. |
| `versions` | number | Number of saved visual versions. |
| `workspaceId` | string | Workspace ID for the visual. |

## Native endpoint

Through the native Columns AI API, this operation is `POST /snapshot/visual` (base URL `https://columns.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-visual-template.md) for the provider-specific parameters and requirements.

