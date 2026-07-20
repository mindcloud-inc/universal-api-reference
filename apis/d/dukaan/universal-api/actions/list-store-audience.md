# Dukaan: List Store Audience

Retrieves store audience records from Dukaan.

```
GET https://connect.mindcloud.co/v1/universal/dukaan/latest/actions/list-store-audience
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dukaan `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dukaan/latest/actions/list-store-audience?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dukaan/latest/actions/list-store-audience?${params}`, {
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
      "address_line": "string",
      "city": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "id": 1,
      "mobile": "string",
      "modified_at": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "notes": "string",
      "orders_count": 1,
      "orders_total_cost": 1,
      "pin": "string",
      "state": "string",
      "tags": [
        {}
      ],
      "type": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address_line` | string | Customer address line |
| `city` | string | Customer city |
| `created_at` | date | Creation timestamp |
| `email` | string | Customer email address |
| `id` | number | Dukaan customer or audience record ID |
| `mobile` | string | Customer mobile number |
| `modified_at` | date | Last modified timestamp |
| `name` | string | Customer name |
| `notes` | string | Customer notes |
| `orders_count` | number | Customer order count |
| `orders_total_cost` | number | Total customer order value |
| `pin` | string | Customer postal code |
| `state` | string | Customer state |
| `tags` | array<object> | Customer tags |
| `type` | string | Customer type |
| `uuid` | string | Dukaan customer UUID |

## Native endpoint

Through the native Dukaan API, this operation is `GET api/store/seller/store-buyer/` (base URL `https://api.mydukaan.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-store-audience.md) for the provider-specific parameters and requirements.

