# Acumatica: List Vendors



```
GET https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/list-vendors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Acumatica `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/list-vendors?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/list-vendors?${params}`, {
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
| `select` | string | no | Comma-separated entity fields to return. Example: `VendorID,VendorName`. |
| `expand` | string | no | Comma-separated detail or linked entities to expand. Example: `MainContact,MainAddress`. |
| `filter` | string | no | Acumatica OData filter expression used to qualify returned records. Example: `VendorID eq 'V000001'`. |
| `custom` | string | no | Comma-separated custom fields to return. Example: `VendorID,VendorName`. |

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
      "APAccount": {
        "value": "string"
      },
      "APSubaccount": {
        "value": "string"
      },
      "CashAccount": {
        "value": "string"
      },
      "CreatedDateTime": {
        "value": "string"
      },
      "CurrencyID": {
        "value": "string"
      },
      "CurrencyRateType": {
        "value": "string"
      },
      "EnableCurrencyOverride": {
        "value": true
      },
      "EnableRateOverride": {
        "value": true
      },
      "F1099Vendor": {
        "value": true
      },
      "ForeignEntity": {
        "value": true
      },
      "id": "string",
      "LandedCostVendor": {
        "value": true
      },
      "LastModifiedDateTime": {
        "value": "string"
      },
      "LocationName": {
        "value": "Ava Chen"
      },
      "MaxReceipt": {
        "value": 1
      },
      "MinReceipt": {
        "value": 1
      },
      "note": {
        "value": "string"
      },
      "PaymentBy": {
        "value": "string"
      },
      "PaymentLeadTimedays": {
        "value": 1
      },
      "PaymentMethod": {
        "value": "string"
      },
      "PaySeparately": {
        "value": true
      },
      "PrintOrders": {
        "value": true
      },
      "ReceiptAction": {
        "value": "string"
      },
      "rowNumber": 1,
      "SendOrdersbyEmail": {
        "value": true
      },
      "Status": {
        "value": "string"
      },
      "Terms": {
        "value": "string"
      },
      "ThresholdReceipt": {
        "value": 1
      },
      "VendorClass": {
        "value": "string"
      },
      "VendorID": {
        "value": "string"
      },
      "VendorIsTaxAgency": {
        "value": true
      },
      "VendorName": {
        "value": "Ava Chen"
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
| `APAccount.value` | string |  |
| `APSubaccount.value` | string |  |
| `CashAccount.value` | string |  |
| `CreatedDateTime.value` | string |  |
| `CurrencyID.value` | string |  |
| `CurrencyRateType.value` | string |  |
| `EnableCurrencyOverride.value` | boolean |  |
| `EnableRateOverride.value` | boolean |  |
| `F1099Vendor.value` | boolean |  |
| `ForeignEntity.value` | boolean |  |
| `id` | string |  |
| `LandedCostVendor.value` | boolean |  |
| `LastModifiedDateTime.value` | string |  |
| `LocationName.value` | string |  |
| `MaxReceipt.value` | number |  |
| `MinReceipt.value` | number |  |
| `note.value` | string |  |
| `PaymentBy.value` | string |  |
| `PaymentLeadTimedays.value` | number |  |
| `PaymentMethod.value` | string |  |
| `PaySeparately.value` | boolean |  |
| `PrintOrders.value` | boolean |  |
| `ReceiptAction.value` | string |  |
| `rowNumber` | number |  |
| `SendOrdersbyEmail.value` | boolean |  |
| `Status.value` | string |  |
| `Terms.value` | string |  |
| `ThresholdReceipt.value` | number |  |
| `VendorClass.value` | string |  |
| `VendorID.value` | string |  |
| `VendorIsTaxAgency.value` | boolean |  |
| `VendorName.value` | string |  |

## Native endpoint

Through the native Acumatica API, this operation is `GET /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/Vendor` (base URL `{{credentials.uRL}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-vendors.md) for the provider-specific parameters and requirements.

