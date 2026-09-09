# Acumatica: List Purchase Receipts



```
GET https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/get-purchase-receipt
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Acumatica `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/get-purchase-receipt?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/get-purchase-receipt?${params}`, {
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
| `select` | string | no | Comma-separated entity fields to return. Example: `ReceiptNbr,Type,Status,VendorID`. |
| `expand` | string | no | Comma-separated detail or linked entities to expand. Example: `Details,OrderDetails`. |
| `filter` | string | no | Acumatica OData filter expression used to qualify returned records. Example: `Status eq 'Open'`. |
| `custom` | string | no | Comma-separated custom fields to return. Example: `ReceiptNbr,Status`. |

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
      "BaseCurrencyID": {
        "value": "string"
      },
      "BillDate": {
        "value": "string"
      },
      "Branch": {
        "value": "string"
      },
      "ControlQty": {
        "value": 1
      },
      "CreateBill": {
        "value": true
      },
      "CurrencyEffectiveDate": {
        "value": "string"
      },
      "CurrencyID": {
        "value": "string"
      },
      "CurrencyRate": {
        "value": 1
      },
      "CurrencyRateTypeID": {
        "value": "string"
      },
      "CurrencyReciprocalRate": {
        "value": 1
      },
      "Date": {
        "value": "string"
      },
      "Hold": {
        "value": true
      },
      "id": "string",
      "Location": {
        "value": "string"
      },
      "note": {
        "value": "string"
      },
      "PostPeriod": {
        "value": "string"
      },
      "ProcessReturnWithOriginalCost": {
        "value": true
      },
      "ReceiptNbr": {
        "value": "string"
      },
      "rowNumber": 1,
      "Status": {
        "value": "string"
      },
      "TotalCost": {
        "value": 1
      },
      "TotalQty": {
        "value": 1
      },
      "Type": {
        "value": "string"
      },
      "UnbilledQuantity": {
        "value": 1
      },
      "VendorID": {
        "value": "string"
      },
      "VendorRef": {
        "value": "string"
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
| `BaseCurrencyID.value` | string |  |
| `BillDate.value` | string |  |
| `Branch.value` | string |  |
| `ControlQty.value` | number |  |
| `CreateBill.value` | boolean |  |
| `CurrencyEffectiveDate.value` | string |  |
| `CurrencyID.value` | string |  |
| `CurrencyRate.value` | number |  |
| `CurrencyRateTypeID.value` | string |  |
| `CurrencyReciprocalRate.value` | number |  |
| `Date.value` | string |  |
| `Hold.value` | boolean |  |
| `id` | string |  |
| `Location.value` | string |  |
| `note.value` | string |  |
| `PostPeriod.value` | string |  |
| `ProcessReturnWithOriginalCost.value` | boolean |  |
| `ReceiptNbr.value` | string |  |
| `rowNumber` | number |  |
| `Status.value` | string |  |
| `TotalCost.value` | number |  |
| `TotalQty.value` | number |  |
| `Type.value` | string |  |
| `UnbilledQuantity.value` | number |  |
| `VendorID.value` | string |  |
| `VendorRef.value` | string |  |

## Native endpoint

Through the native Acumatica API, this operation is `GET /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/PurchaseReceipt` (base URL `{{credentials.uRL}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-purchase-receipt.md) for the provider-specific parameters and requirements.

