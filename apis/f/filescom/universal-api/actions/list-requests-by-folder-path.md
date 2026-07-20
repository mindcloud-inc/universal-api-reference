# Files.com: List Requests by Folder Path

Retrieves requests for a folder path from Files.com.

```
GET https://connect.mindcloud.co/v1/universal/filescom/latest/actions/list-requests-by-folder-path
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Files.com `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/filescom/latest/actions/list-requests-by-folder-path?connectionId=$CONNECTION_ID&limit=25&offset=0&path=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "path": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/filescom/latest/actions/list-requests-by-folder-path?${params}`, {
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
| `mine` | boolean | no | When true, return only requests owned by the current Files.com user. |
| `path` | string | yes | Folder path without leading or trailing slashes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "automation_id": 1,
      "destination": "string",
      "group_ids": "string",
      "id": 1,
      "path": "string",
      "source": "string",
      "user_display_name": "Ava Chen",
      "user_ids": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `automation_id` | number |  |
| `destination` | string |  |
| `group_ids` | string |  |
| `id` | number |  |
| `path` | string |  |
| `source` | string |  |
| `user_display_name` | string |  |
| `user_ids` | string |  |

## Native endpoint

Through the native Files.com API, this operation is `GET /requests/folders/:path` (base URL `{{credentials.siteUrl}}/api/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-requests-by-folder-path.md) for the provider-specific parameters and requirements.

