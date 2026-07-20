# Browser Use: Create Workspace File Upload URLs

Retrieves presigned upload URLs for workspace files from Browser Use.

```
POST https://connect.mindcloud.co/v1/universal/browserUse/latest/actions/create-workspace-file-upload-urls
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Browser Use `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/browserUse/latest/actions/create-workspace-file-upload-urls" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "files[]": [
    {}
  ],
  "workspaceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/browserUse/latest/actions/create-workspace-file-upload-urls', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "files[]": [{}],
    "workspaceId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `files[]` | array<object> | yes | Files to upload. Each item should include the workspace-relative path or file metadata accepted by Browser Use. |
| `workspaceId` | string | yes | Workspace ID. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `prefix` | string | no | Directory prefix to upload into, such as uploads/. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "files": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `files` | array<object> |  |

## Native endpoint

Through the native Browser Use API, this operation is `POST /workspaces/:workspace_id/files/upload` (base URL `https://api.browser-use.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-workspace-file-upload-urls.md) for the provider-specific parameters and requirements.

