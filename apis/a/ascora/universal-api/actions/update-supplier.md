# Ascora: Update Supplier

Updates an existing supplier in Ascora.

```
PUT https://connect.mindcloud.co/v1/universal/ascora/latest/actions/update-supplier
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ascora `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ascora/latest/actions/update-supplier" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "supplierId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ascora/latest/actions/update-supplier', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "supplierId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `businessNumber` | string | no | Business number such as ABN. |
| `emailAddress` | string | no | Email address. |
| `mobile` | string | no | Mobile number. |
| `name` | string | yes | Supplier name. |
| `notes` | string | no | Supplier notes. |
| `phone` | string | no | Phone number. |
| `streetLine1` | string | no | Street address line 1. |
| `streetPostcode` | string | no | Street postcode. |
| `streetState` | string | no | Street state. |
| `streetSuburb` | string | no | Street suburb. |
| `supplierId` | string | yes | Existing supplier ID to update. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true,
      "supplier": {
        "businessNumber": "string",
        "contactFirstName": "Ava",
        "contactLastName": "Chen",
        "emailAddress": "ava@example.com",
        "expenseAccount": "string",
        "fax": "string",
        "invoiceDueDaysType": 1,
        "mobile": "string",
        "name": "Ava Chen",
        "notes": "string",
        "phone": "string",
        "postalLine1": "string",
        "postalLine2": "string",
        "postalPostcode": "string",
        "postalState": "string",
        "postalSuburb": "string",
        "streetLine1": "string",
        "streetLine2": "string",
        "streetPostcode": "string",
        "streetState": "string",
        "streetSuburb": "string",
        "supplierId": "string",
        "supplierNumber": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |
| `supplier.businessNumber` | string |  |
| `supplier.contactFirstName` | string |  |
| `supplier.contactLastName` | string |  |
| `supplier.emailAddress` | string |  |
| `supplier.expenseAccount` | string |  |
| `supplier.fax` | string |  |
| `supplier.invoiceDueDaysType` | number |  |
| `supplier.mobile` | string |  |
| `supplier.name` | string |  |
| `supplier.notes` | string |  |
| `supplier.phone` | string |  |
| `supplier.postalLine1` | string |  |
| `supplier.postalLine2` | string |  |
| `supplier.postalPostcode` | string |  |
| `supplier.postalState` | string |  |
| `supplier.postalSuburb` | string |  |
| `supplier.streetLine1` | string |  |
| `supplier.streetLine2` | string |  |
| `supplier.streetPostcode` | string |  |
| `supplier.streetState` | string |  |
| `supplier.streetSuburb` | string |  |
| `supplier.supplierId` | string |  |
| `supplier.supplierNumber` | string |  |

## Native endpoint

Through the native Ascora API, this operation is `POST /Suppliers/Supplier` (base URL `https://api.ascora.com.au`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-supplier.md) for the provider-specific parameters and requirements.

