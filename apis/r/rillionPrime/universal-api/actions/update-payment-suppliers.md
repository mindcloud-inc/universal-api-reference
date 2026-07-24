# Rillion Prime Pay: Update Payment Suppliers



```
PUT https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/update-payment-suppliers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime Pay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/update-payment-suppliers" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "suppliers[]": [
    {}
  ],
  "suppliers[].supplierId": "string",
  "suppliers[].syncWithPaymentProvider": "false"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/update-payment-suppliers', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "suppliers[]": [{}],
    "suppliers[].supplierId": "string",
    "suppliers[].syncWithPaymentProvider": "false"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `suppliers[]` | array<object> | yes | Array of suppliers to update |
| `suppliers[].supplierId` | string | yes | Unique supplier Id |
| `suppliers[].syncWithPaymentProvider` | boolean | yes | Boolean indicator to decide if Supplier needs to sync with payment provider Default: `false`. |
| `suppliers[].supplierstatus` | list<string> | no | Status of the supplier One of: `PayDisabled`, `PayEnabled`, `RemitAddressNeeded`. |
| `suppliers[].supplierRemitAddress` | object | no | Remit address for the supplier |
| `suppliers[].supplierRemitAddress.street1` | string | no | Street address line 1 |
| `suppliers[].supplierRemitAddress.street2` | string | no | Street address line 2 |
| `suppliers[].supplierRemitAddress.postalCode` | string | no | Postal Code |
| `suppliers[].supplierRemitAddress.zipCode` | string | no | Zip Code |
| `suppliers[].supplierRemitAddress.city` | string | no | City |
| `suppliers[].supplierRemitAddress.state` | string | no | State |
| `suppliers[].supplierRemitAddress.country` | string | no | Country |
| `suppliers[].supplierRemitAddress.careOf` | string | no | CareOf |
| `suppliers[].supplierPaymentGrouping` | list<string> | no | Payment grouping option for the supplier One of: `Bundle`, `SendIndividually`. |
| `suppliers[].isInternational` | boolean | no | Indicates if the supplier is an international supplier |
| `suppliers[].internationalDetails` | object | no | International payment details for the supplier |
| `suppliers[].internationalDetails.currency` | string | no | Currency code |
| `suppliers[].internationalDetails.iban` | string | no | International Bank Account Number |
| `suppliers[].internationalDetails.swift` | string | no | SWIFT/BIC code |
| `suppliers[].internationalDetails.accountNumber` | string | no | Bank account number |
| `suppliers[].internationalDetails.routingCode` | string | no | Routing code |
| `suppliers[].internationalDetails.clabe` | string | no | CLABE number (Mexico) |
| `suppliers[].internationalDetails.bankName` | string | no | Name of the bank |
| `suppliers[].internationalDetails.bankCountry` | string | no | Country of the bank |
| `suppliers[].internationalDetails.remittanceEmail` | string | no | Email for remittance advice |
| `suppliers[].internationalDetails.phoneNo` | string | no | Phone number |
| `suppliers[].internationalDetails.payeeType` | string | no | Type of payee |
| `suppliers[].internationalDetails.purpose` | string | no | Purpose of payment |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rillion Prime Pay API returns.

## Native endpoint

Through the native Rillion Prime Pay API, this operation is `PUT /payment/suppliers` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-payment-suppliers.md) for the provider-specific parameters and requirements.

