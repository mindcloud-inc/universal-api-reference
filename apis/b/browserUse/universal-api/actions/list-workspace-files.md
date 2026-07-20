# Browser Use: List Workspace Files

Retrieves workspace files from Browser Use.

```
GET https://connect.mindcloud.co/v1/universal/browserUse/latest/actions/list-workspace-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Browser Use `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/browserUse/latest/actions/list-workspace-files?connectionId=$CONNECTION_ID&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/browserUse/latest/actions/list-workspace-files?${params}`, {
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
| `workspaceId` | string | yes | Workspace ID. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cursor` | string | no | Pagination cursor. |
| `includeUrls` | boolean | no | Whether to include presigned download URLs. Default: `false`. |
| `limit` | number | no | Maximum number of files to return. Default: `50`. |
| `prefix` | string | no | Directory prefix to list. |
| `shallow` | boolean | no | Whether to list only immediate children. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "files": [
        {}
      ],
      "folders": [
        "string"
      ],
      "hasMore": true,
      "nextCursor": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `files` | array<object> |  |
| `folders` | array<string> |  |
| `hasMore` | boolean |  |
| `nextCursor` | string |  |

## Native endpoint

Through the native Browser Use API, this operation is `GET /workspaces/:workspace_id/files` (base URL `https://api.browser-use.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workspace-files.md) for the provider-specific parameters and requirements.

