# YouCan: Get Customer

Retrieves details for a customer from YouCan.

```
GET https://connect.mindcloud.co/v1/universal/youCan/latest/actions/get-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YouCan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/youCan/latest/actions/get-customer?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/youCan/latest/actions/get-customer?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
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
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | array<object> |  |
| `address[].city` | string |  |
| `address[].company` | string |  |
| `address[].country_code` | string |  |
| `address[].country_name` | string |  |
| `address[].created_at` | number |  |
| `address[].default` | boolean |  |
| `address[].first_line` | string |  |
| `address[].first_name` | string |  |
| `address[].full_name` | string |  |
| `address[].id` | string |  |
| `address[].last_name` | string |  |
| `address[].phone` | string |  |
| `address[].region` | string |  |
| `address[].second_line` | string |  |
| `address[].state` | string |  |
| `address[].updated_at` | number |  |
| `address[].zip_code` | string |  |
| `avatar` | string |  |
| `city` | string |  |
| `country` | string |  |
| `created_at` | date |  |
| `deleted_at` | string |  |
| `email` | string |  |
| `first_name` | string |  |
| `full_name` | string |  |
| `id` | string |  |
| `last_name` | string |  |
| `links` | object |  |
| `links.edit` | string |  |
| `location` | string |  |
| `notes` | string |  |
| `phone` | string |  |
| `region` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native YouCan API, this operation is `GET /customers/{id}` (base URL `https://api.youcan.shop`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer.md) for the provider-specific parameters and requirements.

