# Boost: List Files

Retrieves file records available in Boost.

```
GET https://connect.mindcloud.co/v1/universal/boost/latest/actions/list-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Boost `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/boost/latest/actions/list-files?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/boost/latest/actions/list-files?${params}`, {
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
      "created": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "mime": "string",
      "name": "Ava Chen",
      "size": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date | Creation timestamp. |
| `id` | number | File ID. |
| `mime` | string | MIME type. |
| `name` | string | File name. |
| `size` | number | File size. |

## Native endpoint

Through the native Boost API, this operation is `GET /file/` (base URL `https://{{credentials.systemKey}}.boost.space/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-files.md) for the provider-specific parameters and requirements.

