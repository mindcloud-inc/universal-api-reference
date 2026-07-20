# Merit: Create Vendor



```
POST https://connect.mindcloud.co/v1/universal/merit/latest/actions/create-vendor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Merit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/merit/latest/actions/create-vendor" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "countryCode": "EE",
  "vendorType": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/merit/latest/actions/create-vendor', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "countryCode": "EE",
    "vendorType": "1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Vendor name. |
| `countryCode` | string | yes | Two-letter ISO country code. Example: `EE`. |
| `vendorType` | number | yes | 1 for vendor, 3 for reporting entity. Example: `1`. |
| `currencyCode` | string | no | Vendor currency code. Example: `EUR`. |
| `vatAccountable` | boolean | no | Whether the vendor is VAT accountable. |
| `regNo` | string | no | Vendor registration number. |
| `vatRegNo` | string | no | Vendor VAT registration number. |
| `paymentDeadLine` | number | no | Default payment deadline in days. |
| `overDueCharge` | number | no | Default overdue charge percentage. |
| `address` | string | no | Vendor street address. |
| `city` | string | no | Vendor city. |
| `county` | string | no | Vendor county or region. |
| `postalCode` | string | no | Vendor postal code. |
| `phoneNo` | string | no | Primary phone number. |
| `email` | string | no | Vendor email address. Example: `vendor@example.com`. |
| `receiverName` | string | no | Receiver name. |
| `bankAccount` | string | no | Vendor bank account. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Created vendor ID. |
| `name` | string | Created vendor name. |

## Native endpoint

Through the native Merit API, this operation is `POST v2/sendvendor` (base URL `https://aktiva.merit.ee/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-vendor.md) for the provider-specific parameters and requirements.

