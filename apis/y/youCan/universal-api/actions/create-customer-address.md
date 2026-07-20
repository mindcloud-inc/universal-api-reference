# YouCan: Create Customer Address

Creates a customer address in YouCan.

```
POST https://connect.mindcloud.co/v1/universal/youCan/latest/actions/create-customer-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YouCan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/youCan/latest/actions/create-customer-address" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/youCan/latest/actions/create-customer-address', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

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

Through the native YouCan API, this operation is `POST /customers/{id}/addresses` (base URL `https://api.youcan.shop`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer-address.md) for the provider-specific parameters and requirements.

