# Geral: List Pixels

Retrieves pixels from Geral.

```
GET https://connect.mindcloud.co/v1/universal/geral/latest/actions/list-pixels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Geral `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/geral/latest/actions/list-pixels?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/geral/latest/actions/list-pixels?${params}`, {
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
      "datetime": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "last_datetime": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "pixel": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `datetime` | date | Creation timestamp. |
| `id` | number | Pixel ID. |
| `last_datetime` | date | Last update timestamp. |
| `name` | string | Pixel name. |
| `pixel` | string | Pixel identifier. |
| `type` | string | Pixel provider type. |

## Native endpoint

Through the native Geral API, this operation is `GET /pixels/` (base URL `https://ger.al/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-pixels.md) for the provider-specific parameters and requirements.

