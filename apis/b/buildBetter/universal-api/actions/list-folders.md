# BuildBetter: List Folders



```
GET https://connect.mindcloud.co/v1/universal/buildBetter/latest/actions/list-folders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BuildBetter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/buildBetter/latest/actions/list-folders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/buildBetter/latest/actions/list-folders?${params}`, {
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
| `limit` | number | no | Maximum number of folders to return. Default: `25`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "from_project": true,
      "id": "string",
      "is_subfolder": true,
      "name": "Ava Chen",
      "permission": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `from_project` | boolean | Whether the folder comes from a project. |
| `id` | string | BuildBetter folder identifier. |
| `is_subfolder` | boolean | Whether this folder is nested under another folder. |
| `name` | string | Folder name. |
| `permission` | string | Folder permission mode. |
| `updated_at` | date | Last updated timestamp. |

## Native endpoint

Through the native BuildBetter API, this operation is `POST /graphql` (base URL `https://api.buildbetter.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-folders.md) for the provider-specific parameters and requirements.

