# Blaze AI: Get Folder

Retrieves a folder from Blaze AI.

```
GET https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/get-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Blaze AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/get-folder?connectionId=$CONNECTION_ID&workspace_id=994619&id=3413829" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspace_id": "994619",
  "id": "3413829"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/get-folder?${params}`, {
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
| `workspace_id` | number | yes | Default: `994619`. |
| `id` | number | yes | Default: `3413829`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "id": 1,
        "key": "string",
        "parentFolderId": 1,
        "title": "string",
        "workspaceId": 1
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.id` | number |  |
| `data.key` | string |  |
| `data.parentFolderId` | number |  |
| `data.title` | string |  |
| `data.workspaceId` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native Blaze AI API, this operation is `GET /api/v1/w/:workspace_id/folders/:id` (base URL `https://api.blaze.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-folder.md) for the provider-specific parameters and requirements.

