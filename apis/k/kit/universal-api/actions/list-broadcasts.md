# Kit: List Broadcasts

Lists broadcasts in your Kit account.

```
GET https://connect.mindcloud.co/v1/universal/kit/latest/actions/list-broadcasts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kit `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kit/latest/actions/list-broadcasts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kit/latest/actions/list-broadcasts?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `per_page` | number | no | Number of results per page (default 500, max 1000). |
| `after` | string | no | Fetch next page using end_cursor. |
| `before` | string | no | Fetch previous page using start_cursor. |
| `include_total_count` | boolean | no | Include total count in response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "broadcasts": [
        {}
      ],
      "pagination": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `broadcasts` | array<object> | List of broadcasts. |
| `pagination` | object | Cursor pagination metadata. |

## Native endpoint

Through the native Kit API, this operation is `GET /broadcasts` (base URL `https://api.kit.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-broadcasts.md) for the provider-specific parameters and requirements.

