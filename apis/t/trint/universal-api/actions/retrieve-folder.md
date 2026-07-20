# Trint: Retrieve Folder

Retrieves a folder from your Trint account.

```
GET https://connect.mindcloud.co/v1/universal/trint/latest/actions/retrieve-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trint/latest/actions/retrieve-folder?connectionId=$CONNECTION_ID&folderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "folderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trint/latest/actions/retrieve-folder?${params}`, {
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
| `folderId` | string | yes | The folder identifier to retrieve. |
| `workspaceId` | string | no | Shared drive identifier when the folder belongs to a shared drive. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "name": "Ava Chen",
      "parentId": "string",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string | Folder identifier. |
| `name` | string | Folder name. |
| `parentId` | string | Parent folder identifier when the folder is nested. |
| `workspaceId` | string | Shared drive identifier containing the folder. |

## Native endpoint

Through the native Trint API, this operation is `GET /folders/folder` (base URL `https://api.trint.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-folder.md) for the provider-specific parameters and requirements.

