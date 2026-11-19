# SOS Inventory: List Sales Receipts



```
GET https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/list-sales-receipts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SOS Inventory `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/list-sales-receipts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/list-sales-receipts?${params}`, {
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
| `query` | string | no | Match receipt number, comment, customer PO, or customer name. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `status` | list<string> | no | One of: `closed`, `open`. |
| `archived` | list<string> | no | One of: `no`, `yes`. |
| `from` | date | no | Example: `2026-01-01T00:00:00`. |
| `to` | date | no | Example: `2026-01-01T00:00:00`. |
| `location` | list<string> | no |  |
| `channel` | string | no |  |
| `orderStage` | string | no |  |
| `createdSince` | date | no | Example: `2026-01-01T00:00:00`. |
| `updatedSince` | date | no | Example: `2026-01-01T00:00:00`. |
| `summary` | string | no | Any supplied value returns summary fields only. Leave empty for complete records. Example: `yes`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountToken": "string",
      "archived": true,
      "billing": {
        "address": {
          "city": "string",
          "country": "string",
          "stateProvince": "string"
        },
        "addressName": "Ava Chen",
        "addressType": "string",
        "company": "string",
        "contact": "string",
        "email": "ava@example.com",
        "phone": "string"
      },
      "canShip": "string",
      "channel": {
        "id": 1,
        "name": "Ava Chen"
      },
      "closed": true,
      "currency": {
        "id": 1,
        "name": "Ava Chen"
      },
      "customer": {
        "fullname": "Ava Chen",
        "id": 1,
        "name": "Ava Chen"
      },
      "customerMessage": "string",
      "customerNotes": "string",
      "customerPO": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "depositAccount": {
        "id": 1,
        "name": "Ava Chen"
      },
      "depositAmount": 1,
      "discountAmount": 1,
      "discountPercent": 1,
      "discountTaxable": true,
      "dropShip": true,
      "earliestDueDate": "string",
      "exchangeRate": 1,
      "forceSave": true,
      "fsPaymentId": 1,
      "hasSignature": true,
      "id": 1,
      "lastSync": "2026-05-07T12:00:00.000Z",
      "lines": [
        {
          "altAmount": 1,
          "amount": 1,
          "backOrdered": 1,
          "cost": 1,
          "duedate": "string",
          "id": 1,
          "invoiced": 1,
          "item": {
            "id": 1,
            "name": "Ava Chen"
          },
          "lineNumber": 1,
          "margin": 1,
          "picked": 1,
          "produced": 1,
          "quantity": 1,
          "returned": 1,
          "shipped": 1,
          "tax": {
            "taxable": true
          },
          "unitprice": 1,
          "volume": 1,
          "volumeunit": "string",
          "weight": 1,
          "weightunit": "string"
        }
      ],
      "linkedShipments": [
        {
          "id": 1,
          "lineNumber": 1,
          "refNumber": "https://example.com",
          "transactionType": "https://example.com"
        }
      ],
      "location": {
        "id": 1,
        "name": "Ava Chen"
      },
      "number": "string",
      "paymentMethod": {
        "id": 1,
        "name": "Ava Chen",
        "sosPayType": "string",
        "syncToken": 1
      },
      "shipFromAddress": {
        "address": {
          "line1": "string",
          "line2": "string"
        },
        "addressName": "Ava Chen",
        "addressType": "string"
      },
      "shipping": {
        "address": {
          "city": "string",
          "country": "string",
          "stateProvince": "string"
        },
        "addressName": "Ava Chen",
        "addressType": "string",
        "company": "string",
        "contact": "string",
        "email": "ava@example.com",
        "phone": "string"
      },
      "shippingAmount": 1,
      "shippingTaxable": true,
      "starred": 1,
      "statusLink": "https://example.com",
      "statusMessage": "string",
      "storeCustomerToken": true,
      "subTotal": 1,
      "summaryOnly": true,
      "syncMessage": "string",
      "syncToken": 1,
      "taxAmount": 1,
      "taxCode": {
        "id": 1,
        "name": "Ava Chen"
      },
      "taxPercent": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountToken` | string |  |
| `archived` | boolean |  |
| `billing.address.city` | string |  |
| `billing.address.country` | string |  |
| `billing.address.stateProvince` | string |  |
| `billing.addressName` | string |  |
| `billing.addressType` | string |  |
| `billing.company` | string |  |
| `billing.contact` | string |  |
| `billing.email` | string |  |
| `billing.phone` | string |  |
| `canShip` | string |  |
| `channel.id` | number |  |
| `channel.name` | string |  |
| `closed` | boolean |  |
| `currency.id` | number |  |
| `currency.name` | string |  |
| `customer.fullname` | string |  |
| `customer.id` | number |  |
| `customer.name` | string |  |
| `customerMessage` | string |  |
| `customerNotes` | string |  |
| `customerPO` | string |  |
| `date` | date |  |
| `depositAccount.id` | number |  |
| `depositAccount.name` | string |  |
| `depositAmount` | number |  |
| `discountAmount` | number |  |
| `discountPercent` | number |  |
| `discountTaxable` | boolean |  |
| `dropShip` | boolean |  |
| `earliestDueDate` | string |  |
| `exchangeRate` | number |  |
| `forceSave` | boolean |  |
| `fsPaymentId` | number |  |
| `hasSignature` | boolean |  |
| `id` | number |  |
| `lastSync` | date |  |
| `lines` | array<object> |  |
| `lines[].altAmount` | number |  |
| `lines[].amount` | number |  |
| `lines[].backOrdered` | number |  |
| `lines[].cost` | number |  |
| `lines[].duedate` | string |  |
| `lines[].id` | number |  |
| `lines[].invoiced` | number |  |
| `lines[].item.id` | number |  |
| `lines[].item.name` | string |  |
| `lines[].lineNumber` | number |  |
| `lines[].margin` | number |  |
| `lines[].picked` | number |  |
| `lines[].produced` | number |  |
| `lines[].quantity` | number |  |
| `lines[].returned` | number |  |
| `lines[].shipped` | number |  |
| `lines[].tax.taxable` | boolean |  |
| `lines[].unitprice` | number |  |
| `lines[].volume` | number |  |
| `lines[].volumeunit` | string |  |
| `lines[].weight` | number |  |
| `lines[].weightunit` | string |  |
| `linkedShipments` | array<object> |  |
| `linkedShipments[].id` | number |  |
| `linkedShipments[].lineNumber` | number |  |
| `linkedShipments[].refNumber` | string |  |
| `linkedShipments[].transactionType` | string |  |
| `location.id` | number |  |
| `location.name` | string |  |
| `number` | string |  |
| `paymentMethod.id` | number |  |
| `paymentMethod.name` | string |  |
| `paymentMethod.sosPayType` | string |  |
| `paymentMethod.syncToken` | number |  |
| `shipFromAddress.address.line1` | string |  |
| `shipFromAddress.address.line2` | string |  |
| `shipFromAddress.addressName` | string |  |
| `shipFromAddress.addressType` | string |  |
| `shipping.address.city` | string |  |
| `shipping.address.country` | string |  |
| `shipping.address.stateProvince` | string |  |
| `shipping.addressName` | string |  |
| `shipping.addressType` | string |  |
| `shipping.company` | string |  |
| `shipping.contact` | string |  |
| `shipping.email` | string |  |
| `shipping.phone` | string |  |
| `shippingAmount` | number |  |
| `shippingTaxable` | boolean |  |
| `starred` | number |  |
| `statusLink` | string |  |
| `statusMessage` | string |  |
| `storeCustomerToken` | boolean |  |
| `subTotal` | number |  |
| `summaryOnly` | boolean |  |
| `syncMessage` | string |  |
| `syncToken` | number |  |
| `taxAmount` | number |  |
| `taxCode.id` | number |  |
| `taxCode.name` | string |  |
| `taxPercent` | number |  |
| `total` | number |  |

## Native endpoint

Through the native SOS Inventory API, this operation is `GET /api/v2/salesreceipt` (base URL `https://api.sosinventory.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-sales-receipts.md) for the provider-specific parameters and requirements.

