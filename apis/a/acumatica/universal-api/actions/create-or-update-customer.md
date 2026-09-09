# Acumatica: Create or Update Customer



```
PUT https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/create-or-update-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Acumatica `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/create-or-update-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "CustomerID.value": "MCTEST001",
  "CustomerName.value": "MindCloud Test Customer"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/create-or-update-customer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "CustomerID.value": "MCTEST001",
    "CustomerName.value": "MindCloud Test Customer"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `CustomerID` | object | no |  |
| `CustomerID.value` | string | yes | Unique Acumatica customer identifier. Example: `MCTEST001`. |
| `CustomerName` | object | no |  |
| `CustomerName.value` | string | yes | Example: `MindCloud Test Customer`. |
| `CustomerClass` | object | no |  |
| `CustomerClass.value` | string | no | Example: `DEFAULT`. |
| `Status` | object | no |  |
| `Status.value` | string | no | Example: `Active`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `AccountRef` | object | no |  |
| `AccountRef.value` | string | no |  |
| `MainContact` | object | no |  |
| `MainContact.Email` | object | no |  |
| `MainContact.Email.value` | string | no |  |
| `MainContact.Phone1` | object | no |  |
| `MainContact.Phone1.value` | string | no |  |
| `MainContact.Address` | object | no |  |
| `MainContact.Address.AddressLine1` | object | no |  |
| `MainContact.Address.AddressLine1.value` | string | no |  |
| `MainContact.Address.AddressLine2` | object | no |  |
| `MainContact.Address.AddressLine2.value` | string | no |  |
| `MainContact.Address.City` | object | no |  |
| `MainContact.Address.City.value` | string | no |  |
| `MainContact.Address.State` | object | no |  |
| `MainContact.Address.State.value` | string | no |  |
| `MainContact.Address.PostalCode` | object | no |  |
| `MainContact.Address.PostalCode.value` | string | no |  |
| `MainContact.Address.Country` | object | no |  |
| `MainContact.Address.Country.value` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_links": {
        "files:put": "https://example.com",
        "self": "https://example.com"
      },
      "ApplyOverdueCharges": {
        "value": true
      },
      "AutoApplyPayments": {
        "value": true
      },
      "BillingAddressOverride": {
        "value": true
      },
      "BillingContactOverride": {
        "value": true
      },
      "CreatedDateTime": {
        "value": "2026-05-07T12:00:00.000Z"
      },
      "CurrencyID": {
        "value": "string"
      },
      "CustomerClass": {
        "value": "string"
      },
      "CustomerID": {
        "value": "string"
      },
      "CustomerName": {
        "value": "Ava Chen"
      },
      "EnableCurrencyOverride": {
        "value": true
      },
      "EnableRateOverride": {
        "value": true
      },
      "EnableWriteOffs": {
        "value": true
      },
      "id": "string",
      "LastModifiedDateTime": {
        "value": "2026-05-07T12:00:00.000Z"
      },
      "LocationName": {
        "value": "Ava Chen"
      },
      "MultiCurrencyStatements": {
        "value": true
      },
      "note": {
        "value": "string"
      },
      "OrderPriority": {
        "value": 1
      },
      "PrintDunningLetters": {
        "value": true
      },
      "PrintInvoices": {
        "value": true
      },
      "PrintStatements": {
        "value": true
      },
      "ResidentialDelivery": {
        "value": true
      },
      "rowNumber": 1,
      "SaturdayDelivery": {
        "value": true
      },
      "SendDunningLettersbyEmail": {
        "value": true
      },
      "SendInvoicesbyEmail": {
        "value": true
      },
      "SendStatementsbyEmail": {
        "value": true
      },
      "ShippingAddressOverride": {
        "value": true
      },
      "ShippingContactOverride": {
        "value": true
      },
      "ShippingRule": {
        "value": "string"
      },
      "StatementCycleID": {
        "value": "string"
      },
      "StatementType": {
        "value": "string"
      },
      "Status": {
        "value": "string"
      },
      "Terms": {
        "value": "string"
      },
      "WriteOffLimit": {
        "value": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_links.files:put` | string |  |
| `_links.self` | string |  |
| `ApplyOverdueCharges.value` | boolean |  |
| `AutoApplyPayments.value` | boolean |  |
| `BillingAddressOverride.value` | boolean |  |
| `BillingContactOverride.value` | boolean |  |
| `CreatedDateTime.value` | date |  |
| `CurrencyID.value` | string |  |
| `CustomerClass.value` | string |  |
| `CustomerID.value` | string |  |
| `CustomerName.value` | string |  |
| `EnableCurrencyOverride.value` | boolean |  |
| `EnableRateOverride.value` | boolean |  |
| `EnableWriteOffs.value` | boolean |  |
| `id` | string |  |
| `LastModifiedDateTime.value` | date |  |
| `LocationName.value` | string |  |
| `MultiCurrencyStatements.value` | boolean |  |
| `note.value` | string |  |
| `OrderPriority.value` | number |  |
| `PrintDunningLetters.value` | boolean |  |
| `PrintInvoices.value` | boolean |  |
| `PrintStatements.value` | boolean |  |
| `ResidentialDelivery.value` | boolean |  |
| `rowNumber` | number |  |
| `SaturdayDelivery.value` | boolean |  |
| `SendDunningLettersbyEmail.value` | boolean |  |
| `SendInvoicesbyEmail.value` | boolean |  |
| `SendStatementsbyEmail.value` | boolean |  |
| `ShippingAddressOverride.value` | boolean |  |
| `ShippingContactOverride.value` | boolean |  |
| `ShippingRule.value` | string |  |
| `StatementCycleID.value` | string |  |
| `StatementType.value` | string |  |
| `Status.value` | string |  |
| `Terms.value` | string |  |
| `WriteOffLimit.value` | number |  |

## Native endpoint

Through the native Acumatica API, this operation is `PUT /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/Customer` (base URL `{{credentials.uRL}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-customer.md) for the provider-specific parameters and requirements.

