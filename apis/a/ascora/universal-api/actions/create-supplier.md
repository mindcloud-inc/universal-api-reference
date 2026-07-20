# Ascora: Create Supplier

Creates a new supplier in Ascora.

```
POST https://connect.mindcloud.co/v1/universal/ascora/latest/actions/create-supplier
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ascora `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ascora/latest/actions/create-supplier" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Codex Stage3 Supplier"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ascora/latest/actions/create-supplier', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Codex Stage3 Supplier"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name of the supplier. Example: `Codex Stage3 Supplier`. |
| `businessNumber` | string | no | Business number for the supplier, such as an ABN. Example: `11 22 33 44 55`. |
| `notes` | string | no | Notes associated with the supplier. Example: `Created by Codex stage 3 runtime test`. |
| `phone` | string | no | Primary phone number for the supplier. Example: `08 1234 5678`. |
| `mobile` | string | no | Mobile number for the supplier. Example: `0400 000 000`. |
| `emailAddress` | string | no | Email address for the supplier. Example: `supplier@example.com`. |
| `streetLine1` | string | no | Street address line 1 for the supplier. Example: `1 Automation Way`. |
| `streetSuburb` | string | no | Street suburb for the supplier. Example: `Cannington`. |
| `streetState` | string | no | Street state for the supplier. Example: `WA`. |
| `streetPostcode` | string | no | Street postcode for the supplier. Example: `6107`. |

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
        "invoiceDueDaysType": 1,
        "mobile": "string",
        "name": "Ava Chen",
        "notes": "string",
        "phone": "string",
        "streetLine1": "string",
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
| `supplier.invoiceDueDaysType` | number |  |
| `supplier.mobile` | string |  |
| `supplier.name` | string |  |
| `supplier.notes` | string |  |
| `supplier.phone` | string |  |
| `supplier.streetLine1` | string |  |
| `supplier.streetPostcode` | string |  |
| `supplier.streetState` | string |  |
| `supplier.streetSuburb` | string |  |
| `supplier.supplierId` | string |  |
| `supplier.supplierNumber` | string |  |

## Native endpoint

Through the native Ascora API, this operation is `POST /Suppliers/Supplier` (base URL `https://api.ascora.com.au`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-supplier.md) for the provider-specific parameters and requirements.

