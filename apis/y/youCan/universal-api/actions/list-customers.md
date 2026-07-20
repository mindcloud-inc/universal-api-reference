# YouCan: List Customers

Retrieves a list of customers from YouCan.

```
GET https://connect.mindcloud.co/v1/universal/youCan/latest/actions/list-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YouCan `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/youCan/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/youCan/latest/actions/list-customers?${params}`, {
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
| `address` | string | no |  |
| `limit` | string | no |  |
| `orders` | string | no |  |
| `page` | string | no |  |
| `q` | string | no |  |
| `sort_field` | string | no |  |
| `sort_order` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "address": [
            {
              "city": "string",
              "company": "string",
              "country_code": "string",
              "country_name": "Ava Chen",
              "created_at": 1,
              "default": true,
              "first_line": "string",
              "first_name": "Ava",
              "full_name": "Ava Chen",
              "id": "string",
              "last_name": "Chen",
              "phone": "string",
              "region": "string",
              "second_line": "string",
              "state": "string",
              "updated_at": 1,
              "zip_code": "string"
            }
          ],
          "avatar": "string",
          "city": "string",
          "country": "string",
          "created_at": "2026-05-07T12:00:00.000Z",
          "deleted_at": "string",
          "email": "ava@example.com",
          "first_name": "Ava",
          "full_name": "Ava Chen",
          "id": "string",
          "last_name": "Chen",
          "links": {
            "edit": "https://example.com"
          },
          "location": "string",
          "notes": "string",
          "phone": "string",
          "region": "string",
          "updated_at": "2026-05-07T12:00:00.000Z"
        }
      ],
      "meta": {
        "pagination": {
          "count": 1,
          "current_page": 1,
          "links": {
            "next": "https://example.com"
          },
          "per_page": 1,
          "total": 1,
          "total_pages": 1
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `data[].address` | array<object> |  |
| `data[].address[].city` | string |  |
| `data[].address[].company` | string |  |
| `data[].address[].country_code` | string |  |
| `data[].address[].country_name` | string |  |
| `data[].address[].created_at` | number |  |
| `data[].address[].default` | boolean |  |
| `data[].address[].first_line` | string |  |
| `data[].address[].first_name` | string |  |
| `data[].address[].full_name` | string |  |
| `data[].address[].id` | string |  |
| `data[].address[].last_name` | string |  |
| `data[].address[].phone` | string |  |
| `data[].address[].region` | string |  |
| `data[].address[].second_line` | string |  |
| `data[].address[].state` | string |  |
| `data[].address[].updated_at` | number |  |
| `data[].address[].zip_code` | string |  |
| `data[].avatar` | string |  |
| `data[].city` | string |  |
| `data[].country` | string |  |
| `data[].created_at` | date |  |
| `data[].deleted_at` | string |  |
| `data[].email` | string |  |
| `data[].first_name` | string |  |
| `data[].full_name` | string |  |
| `data[].id` | string |  |
| `data[].last_name` | string |  |
| `data[].links` | object |  |
| `data[].links.edit` | string |  |
| `data[].location` | string |  |
| `data[].notes` | string |  |
| `data[].phone` | string |  |
| `data[].region` | string |  |
| `data[].updated_at` | date |  |
| `meta` | object |  |
| `meta.pagination` | object |  |
| `meta.pagination.count` | number |  |
| `meta.pagination.current_page` | number |  |
| `meta.pagination.links` | object |  |
| `meta.pagination.links.next` | string |  |
| `meta.pagination.per_page` | number |  |
| `meta.pagination.total` | number |  |
| `meta.pagination.total_pages` | number |  |

## Native endpoint

Through the native YouCan API, this operation is `GET /customers` (base URL `https://api.youcan.shop`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-customers.md) for the provider-specific parameters and requirements.

