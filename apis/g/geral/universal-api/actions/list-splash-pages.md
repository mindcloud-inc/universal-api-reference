# Geral: List Splash Pages

Retrieves splash pages from Geral.

```
GET https://connect.mindcloud.co/v1/universal/geral/latest/actions/list-splash-pages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Geral `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/geral/latest/actions/list-splash-pages?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/geral/latest/actions/list-splash-pages?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "datetime": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "last_datetime": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string | Splash page color. |
| `datetime` | date | Creation timestamp. |
| `id` | number | Splash page ID. |
| `last_datetime` | date | Last update timestamp. |
| `name` | string | Splash page name. |

## Native endpoint

Through the native Geral API, this operation is `GET /splash-pages/` (base URL `https://ger.al/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-splash-pages.md) for the provider-specific parameters and requirements.

