# Dukaan: Create Warehouse

Creates a new warehouse in Dukaan.

```
POST https://connect.mindcloud.co/v1/universal/dukaan/latest/actions/create-warehouse
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dukaan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dukaan/latest/actions/create-warehouse" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Main Warehouse",
  "contactPersonName": "Suresh",
  "mobileNumber": "9999999991",
  "pincode": "560103",
  "addressLine1": "Warehouse address",
  "city": "Bangalore",
  "state": "Karnataka",
  "country": "in"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dukaan/latest/actions/create-warehouse', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Main Warehouse",
    "contactPersonName": "Suresh",
    "mobileNumber": "9999999991",
    "pincode": "560103",
    "addressLine1": "Warehouse address",
    "city": "Bangalore",
    "state": "Karnataka",
    "country": "in"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Warehouse name. Example: `Main Warehouse`. |
| `contactPersonName` | string | yes | Warehouse contact person name. Example: `Suresh`. |
| `mobileNumber` | string | yes | Warehouse mobile number. Example: `9999999991`. |
| `pincode` | string | yes | Warehouse postal code. Example: `560103`. |
| `addressLine1` | string | yes | Warehouse address line 1. Example: `Warehouse address`. |
| `city` | string | yes | Warehouse city. Example: `Bangalore`. |
| `state` | string | yes | Warehouse state. Example: `Karnataka`. |
| `country` | string | yes | Warehouse country code. Default: `in`. |
| `termsChecked` | boolean | no | Whether terms were checked. Default: `true`. |

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

Through the native Dukaan API, this operation is `POST api/store/seller/store-warehouse/v2/` (base URL `https://api.mydukaan.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-warehouse.md) for the provider-specific parameters and requirements.

