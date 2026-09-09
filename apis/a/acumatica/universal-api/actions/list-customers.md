# Acumatica: List Customers



```
GET https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/list-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Acumatica `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/list-customers?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `select` | string | no | Comma-separated entity fields to return. Example: `CustomerID,CustomerName`. |
| `expand` | string | no | Comma-separated detail or linked entities to expand. Example: `MainContact,MainContact/Address`. |
| `filter` | string | no | Acumatica OData filter expression used to qualify returned records. Example: `CustomerID eq 'ABARTENDE'`. |
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
| `ShippingRule.value` | string |  |
| `StatementCycleID.value` | string |  |
| `StatementType.value` | string |  |
| `Status.value` | string |  |
| `Terms.value` | string |  |
| `WriteOffLimit.value` | number |  |

## Native endpoint

Through the native Acumatica API, this operation is `GET /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/Customer` (base URL `{{credentials.uRL}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-customers.md) for the provider-specific parameters and requirements.

