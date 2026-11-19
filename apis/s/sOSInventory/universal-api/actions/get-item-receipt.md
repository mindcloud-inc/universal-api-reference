# SOS Inventory: Get Item Receipt



```
GET https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/get-item-receipt
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SOS Inventory `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/get-item-receipt?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/get-item-receipt?${params}`, {
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
| `id` | list<number> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "autoSerialLots": true,
      "comment": "string",
      "currency": {
        "id": 1,
        "name": "Ava Chen"
      },
      "customFields": [
        {
          "dataType": "string",
          "id": 1,
          "name": "Ava Chen",
          "value": "string"
        }
      ],
      "date": "2026-05-07T12:00:00.000Z",
      "depositAmount": 1,
      "exchangeRate": 1,
      "hasSignature": true,
      "id": 1,
      "lines": [
        {
          "amount": 1,
          "class": {
            "id": 1,
            "name": "Ava Chen"
          },
          "description": "string",
          "id": 1,
          "item": {
            "id": 1,
            "name": "Ava Chen"
          },
          "lineNumber": 1,
          "linkedTransaction": {
            "id": 1,
            "lineNumber": 1,
            "refNumber": "https://example.com",
            "transactionType": "https://example.com"
          },
          "quantity": 1,
          "received": 1,
          "tax": {
            "taxable": true
          },
          "unitprice": 1,
          "vendorPartNumber": "string",
          "volume": 1,
          "volumeunit": "string",
          "weight": 1,
          "weightunit": "string"
        }
      ],
      "location": {
        "id": 1,
        "name": "Ava Chen"
      },
      "number": "string",
      "overhead": 1,
      "payment": "string",
      "starred": 1,
      "subTotal": 1,
      "summaryOnly": true,
      "syncToken": 1,
      "taxAmount": 1,
      "terms": {
        "id": 1,
        "name": "Ava Chen"
      },
      "total": 1,
      "updateDefaultCosts": true,
      "vendor": {
        "id": 1,
        "name": "Ava Chen"
      },
      "vendorInvoiceDueDate": "2026-05-07T12:00:00.000Z",
      "vendorMessage": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `autoSerialLots` | boolean |  |
| `comment` | string |  |
| `currency.id` | number |  |
| `currency.name` | string |  |
| `customFields` | array<object> |  |
| `customFields[].dataType` | string |  |
| `customFields[].id` | number |  |
| `customFields[].name` | string |  |
| `customFields[].value` | string |  |
| `date` | date |  |
| `depositAmount` | number |  |
| `exchangeRate` | number |  |
| `hasSignature` | boolean |  |
| `id` | number |  |
| `lines` | array<object> |  |
| `lines[].amount` | number |  |
| `lines[].class.id` | number |  |
| `lines[].class.name` | string |  |
| `lines[].description` | string |  |
| `lines[].id` | number |  |
| `lines[].item.id` | number |  |
| `lines[].item.name` | string |  |
| `lines[].lineNumber` | number |  |
| `lines[].linkedTransaction.id` | number |  |
| `lines[].linkedTransaction.lineNumber` | number |  |
| `lines[].linkedTransaction.refNumber` | string |  |
| `lines[].linkedTransaction.transactionType` | string |  |
| `lines[].quantity` | number |  |
| `lines[].received` | number |  |
| `lines[].tax.taxable` | boolean |  |
| `lines[].unitprice` | number |  |
| `lines[].vendorPartNumber` | string |  |
| `lines[].volume` | number |  |
| `lines[].volumeunit` | string |  |
| `lines[].weight` | number |  |
| `lines[].weightunit` | string |  |
| `location.id` | number |  |
| `location.name` | string |  |
| `number` | string |  |
| `overhead` | number |  |
| `payment` | string |  |
| `starred` | number |  |
| `subTotal` | number |  |
| `summaryOnly` | boolean |  |
| `syncToken` | number |  |
| `taxAmount` | number |  |
| `terms.id` | number |  |
| `terms.name` | string |  |
| `total` | number |  |
| `updateDefaultCosts` | boolean |  |
| `vendor.id` | number |  |
| `vendor.name` | string |  |
| `vendorInvoiceDueDate` | date |  |
| `vendorMessage` | string |  |

## Native endpoint

Through the native SOS Inventory API, this operation is `GET /api/v2/itemreceipt/:id` (base URL `https://api.sosinventory.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-item-receipt.md) for the provider-specific parameters and requirements.

