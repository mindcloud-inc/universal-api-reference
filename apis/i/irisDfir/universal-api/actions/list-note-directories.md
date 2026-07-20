# Iris Dfir: List Note Directories



```
GET https://connect.mindcloud.co/v1/universal/irisDfir/latest/actions/list-note-directories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Iris Dfir `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/irisDfir/latest/actions/list-note-directories?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/irisDfir/latest/actions/list-note-directories?${params}`, {
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
      "data": [
        {}
      ],
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Iris Dfir API, this operation is `GET /case/notes/directories/filter` (base URL `https://v200.beta.dfir-iris.org`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-note-directories.md) for the provider-specific parameters and requirements.

