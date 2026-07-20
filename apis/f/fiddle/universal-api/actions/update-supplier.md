# Fiddle: Update Supplier

Updates an existing supplier in Fiddle.

```
PUT https://connect.mindcloud.co/v1/universal/fiddle/latest/actions/update-supplier
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fiddle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/fiddle/latest/actions/update-supplier" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "supplierId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fiddle/latest/actions/update-supplier', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "supplierId": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountRef` | string | no | Account reference |
| `address` | string | no | Supplier address line 1 |
| `address2` | string | no | Supplier address line 2 |
| `city` | string | no | Supplier city |
| `country` | string | no | Supplier country |
| `email` | string | no | Supplier email |
| `fax` | string | no | Supplier fax |
| `mobile` | string | no | Supplier mobile |
| `notes` | string | no | Supplier notes |
| `paymentInfo` | string | no | Payment info |
| `paymentTerms` | string | no | Payment terms |
| `phone` | string | no | Supplier phone |
| `state` | string | no | Supplier state |
| `supplierId` | string | yes | Supplier ID |
| `zip` | string | no | Supplier ZIP or postal code |
| `name` | string | yes | Supplier name |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `disabled` | boolean | no | Whether the supplier is disabled |

## Response

```json
{
  "success": true,
  "data": [
    {
      "supplier": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "id": "string",
        "name": "Ava Chen",
        "updatedAt": "2026-05-07T12:00:00.000Z"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `supplier` | object |  |
| `supplier.createdAt` | date |  |
| `supplier.id` | string |  |
| `supplier.name` | string |  |
| `supplier.updatedAt` | date |  |

## Native endpoint

Through the native Fiddle API, this operation is `PUT /supplier/:supplierId` (base URL `https://fiddle.io/rest/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-supplier.md) for the provider-specific parameters and requirements.

