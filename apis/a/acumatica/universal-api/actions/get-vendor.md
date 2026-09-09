# Acumatica: Get Vendor



```
GET https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/get-vendor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Acumatica `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/get-vendor?connectionId=$CONNECTION_ID&id=e734ff7e-fadb-ea11-8177-c9aeb77cfe99" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "e734ff7e-fadb-ea11-8177-c9aeb77cfe99"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/get-vendor?${params}`, {
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
| `id` | string | yes | The Acumatica entity ID (GUID) returned in the record's id field. Example: `e734ff7e-fadb-ea11-8177-c9aeb77cfe99`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `select` | string | no | Comma-separated entity fields to return. Example: `VendorID,VendorName`. |
| `expand` | string | no | Comma-separated detail or linked entities to expand. Example: `MainContact,MainAddress`. |
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
      "RemittanceAddressOverride": {
        "value": true
      },
      "RemittanceContactOverride": {
        "value": true
      },
      "rowNumber": 1,
      "SendOrdersbyEmail": {
        "value": true
      },
      "ShippingAddressOverride": {
        "value": true
      },
      "ShippingContactOverride": {
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
| `RemittanceAddressOverride.value` | boolean |  |
| `RemittanceContactOverride.value` | boolean |  |
| `rowNumber` | number |  |
| `SendOrdersbyEmail.value` | boolean |  |
| `ShippingAddressOverride.value` | boolean |  |
| `ShippingContactOverride.value` | boolean |  |
| `Status.value` | string |  |
| `Terms.value` | string |  |
| `ThresholdReceipt.value` | number |  |
| `VendorClass.value` | string |  |
| `VendorID.value` | string |  |
| `VendorIsTaxAgency.value` | boolean |  |
| `VendorName.value` | string |  |

## Native endpoint

Through the native Acumatica API, this operation is `GET /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/Vendor/:id` (base URL `{{credentials.uRL}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-vendor.md) for the provider-specific parameters and requirements.

