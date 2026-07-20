# Raklet: List Posts



```
GET https://connect.mindcloud.co/v1/universal/raklet/latest/actions/list-posts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Raklet `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/raklet/latest/actions/list-posts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/raklet/latest/actions/list-posts?${params}`, {
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
| `searchText` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Data": [
        {}
      ],
      "Paging": {
        "Offset": 1,
        "PageSize": 1,
        "ShowingRowCount": 1,
        "TotalRowCount": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Data` | array<object> |  |
| `Paging.Offset` | number |  |
| `Paging.PageSize` | number |  |
| `Paging.ShowingRowCount` | number |  |
| `Paging.TotalRowCount` | number |  |

## Native endpoint

Through the native Raklet API, this operation is `GET /organisations/:organisationId/posts` (base URL `https://api.raklet.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-posts.md) for the provider-specific parameters and requirements.

