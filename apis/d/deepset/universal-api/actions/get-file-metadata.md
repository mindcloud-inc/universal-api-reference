# Deepset: Get File Metadata

Retrieves metadata for a file in Deepset.

```
GET https://connect.mindcloud.co/v1/universal/deepset/latest/actions/get-file-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deepset `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepset/latest/actions/get-file-metadata?connectionId=$CONNECTION_ID&fileId=string&workspaceName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileId": "string",
  "workspaceName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepset/latest/actions/get-file-metadata?${params}`, {
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
| `fileId` | string | yes | deepset file ID. |
| `workspaceName` | string | yes | deepset workspace name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "file_id": "string",
      "meta": {},
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `file_id` | string |  |
| `meta` | object |  |
| `name` | string |  |

## Native endpoint

Through the native Deepset API, this operation is `GET /api/v1/workspaces/:workspace_name/files/:file_id/meta` (base URL `https://api.cloud.deepset.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-file-metadata.md) for the provider-specific parameters and requirements.

