# Fiddle: Create Supplier

Creates a new supplier in Fiddle.

```
POST https://connect.mindcloud.co/v1/universal/fiddle/latest/actions/create-supplier
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fiddle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fiddle/latest/actions/create-supplier" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fiddle/latest/actions/create-supplier', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Supplier name |
| `email` | string | no | Supplier email |
| `phone` | string | no | Supplier phone |
| `address` | string | no | Supplier address line 1 |
| `address2` | string | no | Supplier address line 2 |
| `city` | string | no | Supplier city |
| `state` | string | no | Supplier state |
| `zip` | string | no | Supplier ZIP or postal code |
| `country` | string | no | Supplier country |
| `fax` | string | no | Supplier fax |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `billingAddressInput` | object | no | Billing address object |
| `shippingAddressInput` | object | no | Shipping address object |
| `contacts[]` | array<object> | no | Array of supplier contacts |

## Response

```json
{
  "success": true,
  "data": [
    {
      "suppliers": [
        {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "name": "Ava Chen",
          "updatedAt": "2026-05-07T12:00:00.000Z"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `suppliers` | array<object> |  |
| `suppliers[].createdAt` | date |  |
| `suppliers[].id` | string |  |
| `suppliers[].name` | string |  |
| `suppliers[].updatedAt` | date |  |

## Native endpoint

Through the native Fiddle API, this operation is `POST /suppliers` (base URL `https://fiddle.io/rest/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-supplier.md) for the provider-specific parameters and requirements.

