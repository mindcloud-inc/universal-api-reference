# Dukaan: List Warehouses

Retrieves warehouses from Dukaan.

```
GET https://connect.mindcloud.co/v1/universal/dukaan/latest/actions/list-warehouses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dukaan `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dukaan/latest/actions/list-warehouses?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dukaan/latest/actions/list-warehouses?${params}`, {
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
      "address_line_1": "string",
      "address_line_2": "string",
      "city": "string",
      "contact_person_name": "Ava Chen",
      "country": {},
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "is_active": true,
      "is_primary_warehouse": true,
      "mobile_number": "string",
      "modified_at": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "pincode": "string",
      "state": "string",
      "store": 1,
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address_line_1` | string | Warehouse address line 1 |
| `address_line_2` | string | Warehouse address line 2 |
| `city` | string | Warehouse city |
| `contact_person_name` | string | Warehouse contact person |
| `country` | object | Warehouse country details |
| `created_at` | date | Creation timestamp |
| `id` | number | Dukaan warehouse ID |
| `is_active` | boolean | Whether the warehouse is active |
| `is_primary_warehouse` | boolean | Whether this is the primary warehouse |
| `mobile_number` | string | Warehouse contact mobile number |
| `modified_at` | date | Last modified timestamp |
| `name` | string | Warehouse name |
| `pincode` | string | Warehouse postal code |
| `state` | string | Warehouse state |
| `store` | number | Dukaan store ID |
| `uuid` | string | Dukaan warehouse UUID |

## Native endpoint

Through the native Dukaan API, this operation is `GET api/store/seller/store-warehouse/v2/` (base URL `https://api.mydukaan.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-warehouses.md) for the provider-specific parameters and requirements.

