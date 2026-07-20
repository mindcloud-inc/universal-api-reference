# Files.com: List Login History

Retrieves site login history from Files.com.

```
GET https://connect.mindcloud.co/v1/universal/filescom/latest/actions/list-login-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Files.com `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/filescom/latest/actions/list-login-history?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/filescom/latest/actions/list-login-history?${params}`, {
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
| `cursor` | string | no | Cursor token returned by a previous login-history response page. |
| `display` | string | no | Optional display mode. Files.com supports `full` or `parent`. |
| `endAt` | date | no | Return login history entries at or before this timestamp. |
| `perPage` | number | no | Maximum number of items to return in one page. |
| `perPage` | string | no | Maximum number of login history entries to return in one page. |
| `startAt` | date | no | Return login history entries at or after this timestamp. |
| `cursor` | string | no | Cursor token returned by a previous page. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "action": "string",
      "id": 1,
      "interface": "string",
      "ip": "string",
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
| `id` | number |  |
| `interface` | string |  |
| `ip` | string |  |
| `user_id` | number |  |
| `username` | string |  |
| `when` | date |  |

## Native endpoint

Through the native Files.com API, this operation is `GET /history/login` (base URL `{{credentials.siteUrl}}/api/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-login-history.md) for the provider-specific parameters and requirements.

