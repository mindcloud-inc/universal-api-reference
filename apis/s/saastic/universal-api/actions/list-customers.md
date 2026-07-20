# Saastic: List Customers

Retrieves customers from Saastic.

```
GET https://connect.mindcloud.co/v1/universal/saastic/latest/actions/list-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Saastic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/saastic/latest/actions/list-customers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/saastic/latest/actions/list-customers?${params}`, {
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
      "charges_count": 1,
      "charges_sum": 1,
      "city": "string",
      "company": "string",
      "created_at": 1,
      "email": "ava@example.com",
      "first_name": "Ava",
      "has_subscription": 1,
      "id": 1,
      "last_name": "Chen",
      "location_id": 1,
      "name": "Ava Chen",
      "phone": "string",
      "postal_code": "string",
      "review_link": "https://example.com",
      "state": "string",
      "updated_at": 1,
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `charges_count` | number |  |
| `charges_sum` | number |  |
| `city` | string |  |
| `company` | string |  |
| `created_at` | number |  |
| `email` | string |  |
| `first_name` | string |  |
| `has_subscription` | number |  |
| `id` | number |  |
| `last_name` | string |  |
| `location_id` | number |  |
| `name` | string |  |
| `phone` | string |  |
| `postal_code` | string |  |
| `review_link` | string |  |
| `state` | string |  |
| `updated_at` | number |  |
| `uuid` | string |  |

## Native endpoint

Through the native Saastic API, this operation is `GET /beacon/customers` (base URL `https://api.moregoodreviews.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-customers.md) for the provider-specific parameters and requirements.

