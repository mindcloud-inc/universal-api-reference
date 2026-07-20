# Files.com: List History

Retrieves site action history from Files.com.

```
GET https://connect.mindcloud.co/v1/universal/filescom/latest/actions/list-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Files.com `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/filescom/latest/actions/list-history?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/filescom/latest/actions/list-history?${params}`, {
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
| `cursor` | string | no | Cursor token returned by a previous history response page. |
| `display` | string | no | Optional display mode. Files.com supports `full` or `parent`. |
| `endAt` | date | no | Return history entries at or before this timestamp. |
| `perPage` | number | no | Maximum number of items to return in one page. |
| `perPage` | number | no | Maximum number of history entries to return in one page. |
| `startAt` | date | no | Return history entries at or after this timestamp. |
| `cursor` | string | no | Cursor token returned by a previous page. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "action": "string",
      "destination": "string",
      "id": 1,
      "interface": "string",
      "path": "string",
      "source": "string",
      "user_id": 1,
      "username": "Ava Chen",
      "when": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action` | string |  |
| `destination` | string |  |
| `id` | number |  |
| `interface` | string |  |
| `path` | string |  |
| `source` | string |  |
| `user_id` | number |  |
| `username` | string |  |
| `when` | date |  |

## Native endpoint

Through the native Files.com API, this operation is `GET /history` (base URL `{{credentials.siteUrl}}/api/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-history.md) for the provider-specific parameters and requirements.

