# Rillion Prime Pay: Update Payment Supplier



```
PUT https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/update-payment-supplier
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime Pay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/update-payment-supplier" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "supplierId": "string",
  "syncWithPaymentProvider": "false"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/update-payment-supplier', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "supplierId": "string",
    "syncWithPaymentProvider": "false"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `xCorrelationId` | string | no |  |
| `supplierId` | string | yes | Unique supplier Id |
| `syncWithPaymentProvider` | boolean | yes | Boolean indicator to decide if Supplier needs to sync with payment provider Default: `false`. |
| `supplierstatus` | list<string> | no | Status of the supplier One of: `PayDisabled`, `PayEnabled`, `RemitAddressNeeded`. |
| `supplierRemitAddress` | object | no | Remit address for the supplier |
| `supplierPaymentGrouping` | list<list> | no | Payment grouping option for the supplier One of: `Bundle`, `SendIndividually`. |
| `supplierRemitAddress.street1` | string | no | Street address line 1 |
| `isInternational` | boolean | no | Indicates if the supplier is an international supplier |
| `supplierRemitAddress.street2` | string | no | Street address line 2 |
| `internationalDetails` | object | no | International payment details for the supplier |
| `supplierRemitAddress.postalCode` | string | no | Postal Code |
| `supplierRemitAddress.zipCode` | string | no | Zip Code |
| `supplierRemitAddress.city` | string | no | City |
| `supplierRemitAddress.state` | string | no | State |
| `supplierRemitAddress.country` | string | no | Country |
| `supplierRemitAddress.careOf` | string | no | CareOf |
| `internationalDetails.currency` | string | no | Currency code |
| `internationalDetails.iban` | string | no | International Bank Account Number |
| `internationalDetails.swift` | string | no | SWIFT/BIC code |
| `internationalDetails.accountNumber` | string | no | Bank account number |
| `internationalDetails.routingCode` | string | no | Routing code |
| `internationalDetails.clabe` | string | no | CLABE number (Mexico) |
| `internationalDetails.bankName` | string | no | Name of the bank |
| `internationalDetails.bankCountry` | string | no | Country of the bank |
| `internationalDetails.remittanceEmail` | string | no | Email for remittance advice |
| `internationalDetails.phoneNo` | string | no | Phone number |
| `internationalDetails.payeeType` | string | no | Type of payee |
| `internationalDetails.purpose` | string | no | Purpose of payment |
| `internationalDetails.branchCode` | string | no | Branch code |
| `internationalDetails.accountType` | string | no | Account type |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rillion Prime Pay API returns.

## Native endpoint

Through the native Rillion Prime Pay API, this operation is `PUT /payment/supplier` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-payment-supplier.md) for the provider-specific parameters and requirements.

