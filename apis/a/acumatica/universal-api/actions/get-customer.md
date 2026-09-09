# Acumatica: Get Customer



```
GET https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/get-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Acumatica `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/get-customer?connectionId=$CONNECTION_ID&id=01a0c017-df7f-ea11-8175-b9d61cb73193" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "01a0c017-df7f-ea11-8175-b9d61cb73193"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/get-customer?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The Acumatica entity ID (GUID) returned in the record's id field. Example: `01a0c017-df7f-ea11-8175-b9d61cb73193`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `select` | string | no | Comma-separated entity fields to return. Example: `CustomerID,CustomerName`. |
| `expand` | string | no | Comma-separated detail or linked entities to expand. Example: `MainContact,MainContact/Address`. |
| `custom` | string | no | Comma-separated custom fields to return. Example: `CustomerID,CustomerName`. |

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
        "value": "string"
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
        "value": "string"
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
| `CreatedDateTime.value` | string |  |
| `CurrencyID.value` | string |  |
| `CustomerClass.value` | string |  |
| `CustomerID.value` | string |  |
| `CustomerName.value` | string |  |
| `EnableCurrencyOverride.value` | boolean |  |
| `EnableRateOverride.value` | boolean |  |
| `EnableWriteOffs.value` | boolean |  |
| `id` | string |  |
| `LastModifiedDateTime.value` | string |  |
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

Through the native Acumatica API, this operation is `GET /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/Customer/:id` (base URL `{{credentials.uRL}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer.md) for the provider-specific parameters and requirements.

