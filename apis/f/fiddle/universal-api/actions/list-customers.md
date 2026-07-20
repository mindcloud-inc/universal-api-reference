# Fiddle: List Customers

Retrieves customer records from the Fiddle account.

```
GET https://connect.mindcloud.co/v1/universal/fiddle/latest/actions/list-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fiddle `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fiddle/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fiddle/latest/actions/list-customers?${params}`, {
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
| `page` | number | no | Page number |
| `size` | number | no | Page size |
| `query` | string | no | Customer search query |
| `status` | string | no | Customer status filter |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sortBy` | string | no | Sort field |
| `sortDirection` | string | no | Sort direction |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customers": [
        {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "name": "Ava Chen",
          "updatedAt": "2026-05-07T12:00:00.000Z"
        }
      ],
      "meta": {
        "count": 1,
        "from": 1,
        "lastPage": 1,
        "page": 1,
        "query": "string",
        "size": 1,
        "sortBy": "string",
        "sortDirection": "string",
        "to": 1,
        "total": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customers` | array<object> |  |
| `customers[].createdAt` | date |  |
| `customers[].id` | string |  |
| `customers[].name` | string |  |
| `customers[].updatedAt` | date |  |
| `meta` | object |  |
| `meta.count` | number |  |
| `meta.from` | number |  |
| `meta.lastPage` | number |  |
| `meta.page` | number |  |
| `meta.query` | string |  |
| `meta.size` | number |  |
| `meta.sortBy` | string |  |
| `meta.sortDirection` | string |  |
| `meta.to` | number |  |
| `meta.total` | number |  |

## Native endpoint

Through the native Fiddle API, this operation is `GET /customers` (base URL `https://fiddle.io/rest/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-customers.md) for the provider-specific parameters and requirements.

