# Files.com: Delete File or Folder

Deletes a file or folder from Files.com.

```
DELETE https://connect.mindcloud.co/v1/universal/filescom/latest/actions/delete-file-or-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Files.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/filescom/latest/actions/delete-file-or-folder?connectionId=$CONNECTION_ID&path=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "path": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/filescom/latest/actions/delete-file-or-folder?${params}`, {
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
| `path` | string | yes | File or folder path to delete, without leading or trailing slashes. |
| `recursive` | boolean | no | Delete folder contents recursively when true. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Files.com API returns.

## Native endpoint

Through the native Files.com API, this operation is `DELETE /files/:path` (base URL `{{credentials.siteUrl}}/api/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-file-or-folder.md) for the provider-specific parameters and requirements.

