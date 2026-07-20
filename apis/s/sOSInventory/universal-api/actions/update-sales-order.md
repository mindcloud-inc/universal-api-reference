# SOS Inventory: Update Sales Order

Updates an existing sales order in SOS Inventory.

```
PUT https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/update-sales-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SOS Inventory `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/update-sales-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "syncTokenValue": "string",
  "salesOrderBodyId": 1,
  "number": "string",
  "date": "string",
  "customer.id": 1,
  "location.id": 1,
  "lines[].item.id": 1,
  "lines[].quantity": 1,
  "lines[].unitPrice": 1,
  "lines[].amount": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/update-sales-order', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "syncTokenValue": "string",
    "salesOrderBodyId": 1,
    "number": "string",
    "date": "string",
    "customer.id": 1,
    "location.id": 1,
    "lines[].item.id": 1,
    "lines[].quantity": 1,
    "lines[].unitPrice": 1,
    "lines[].amount": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Unique identifier for this record. |
| `syncTokenValue` | string | yes | Current version token for this record. |
| `salesOrderBodyId` | number | yes | The sales order id echoed in the request body. |
| `number` | string | yes | Order number for this sales order. |
| `date` | string | yes | Transaction date. |
| `customer.id` | number | yes | Customer for this transaction. |
| `location.id` | number | yes | Location for this transaction. |
| `customerMessage` | string | no | Customer message field. |
| `comment` | string | no | Internal comment for this transaction. |
| `lines[].item.id` | number | yes | The item this line represents. |
| `lines[].quantity` | number | yes | The quantity for this line item. |
| `lines[].unitPrice` | number | yes | The unit price for this item. |
| `lines[].amount` | number | yes | The amount for this line item. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountToken": "string",
      "archived": true,
      "assignedToUser": {},
      "billing": {
        "address": {
          "city": {},
          "country": {},
          "line1": {},
          "line2": {},
          "line3": {},
          "line4": {},
          "line5": {},
          "postalCode": {},
          "stateProvince": {}
        },
        "addressName": "Ava Chen",
        "addressType": "string",
        "company": {},
        "contact": {},
        "email": {},
        "phone": {}
      },
      "channel": {},
      "closed": true,
      "comment": "string",
      "currency": {},
      "customer": {
        "id": 1,
        "name": "Ava Chen"
      },
      "customerMessage": "string",
      "customerNotes": "string",
      "customerPO": "string",
      "customFields": {},
      "date": "string",
      "department": {},
      "depositAmount": 1,
      "discountAmount": 1,
      "discountPercent": 1,
      "discountTaxable": true,
      "dropShip": true,
      "earliestDueDate": "string",
      "exchangeRate": 1,
      "forceSave": true,
      "hasSignature": true,
      "id": 1,
      "keys": {},
      "lines": [
        {
          "altAmount": 1,
          "amount": 1,
          "backOrdered": 1,
          "bin": {},
          "class": {},
          "cost": {},
          "description": "string",
          "duedate": "string",
          "id": 1,
          "invoiced": 1,
          "item": {
            "id": 1,
            "name": "Ava Chen"
          },
          "job": {},
          "lineNumber": 1,
          "linkedTransaction": {},
          "listPrice": {},
          "lot": {},
          "margin": {},
          "percentdiscount": {},
          "picked": 1,
          "produced": 1,
          "quantity": 1,
          "returned": 1,
          "serials": {},
          "shipped": 1,
          "tax": {
            "taxable": true,
            "taxCode": {},
            "taxExemptReasonId": {}
          },
          "unitprice": 1,
          "uom": {},
          "volume": 1,
          "volumeunit": "string",
          "weight": 1,
          "weightunit": "string",
          "workcenter": {}
        }
      ],
      "linkedTransaction": {},
      "location": {
        "id": 1,
        "name": "Ava Chen"
      },
      "number": "string",
      "orderStage": {},
      "priority": {},
      "salesRep": {},
      "serial": {},
      "shipping": {
        "address": {
          "city": {},
          "country": {},
          "line1": {},
          "line2": {},
          "line3": {},
          "line4": {},
          "line5": {},
          "postalCode": {},
          "stateProvince": {}
        },
        "addressName": "Ava Chen",
        "addressType": "string",
        "company": {},
        "contact": {},
        "email": {},
        "phone": {}
      },
      "shippingAmount": 1,
      "shippingTaxable": true,
      "starred": 1,
      "statusLink": "https://example.com",
      "statusMessage": "string",
      "storeCustomerToken": true,
      "subTotal": 1,
      "summaryOnly": true,
      "syncToken": 1,
      "taxAmount": 1,
      "taxCode": {},
      "taxPercent": 1,
      "terms": {},
      "total": 1,
      "transactionLocationQuickBooks": "string",
      "values": {}
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
| `assignedToUser` | object |  |
| `billing.address.city` | object |  |
| `billing.address.country` | object |  |
| `billing.address.line1` | object |  |
| `billing.address.line2` | object |  |
| `billing.address.line3` | object |  |
| `billing.address.line4` | object |  |
| `billing.address.line5` | object |  |
| `billing.address.postalCode` | object |  |
| `billing.address.stateProvince` | object |  |
| `billing.addressName` | string |  |
| `billing.addressType` | string |  |
| `billing.company` | object |  |
| `billing.contact` | object |  |
| `billing.email` | object |  |
| `billing.phone` | object |  |
| `channel` | object |  |
| `closed` | boolean |  |
| `comment` | string |  |
| `currency` | object |  |
| `customer.id` | number |  |
| `customer.name` | string |  |
| `customerMessage` | string |  |
| `customerNotes` | string |  |
| `customerPO` | string |  |
| `customFields` | object |  |
| `date` | string |  |
| `department` | object |  |
| `depositAmount` | number |  |
| `discountAmount` | number |  |
| `discountPercent` | number |  |
| `discountTaxable` | boolean |  |
| `dropShip` | boolean |  |
| `earliestDueDate` | string |  |
| `exchangeRate` | number |  |
| `forceSave` | boolean |  |
| `hasSignature` | boolean |  |
| `id` | number |  |
| `keys` | object |  |
| `lines[].altAmount` | number |  |
| `lines[].amount` | number |  |
| `lines[].backOrdered` | number |  |
| `lines[].bin` | object |  |
| `lines[].class` | object |  |
| `lines[].cost` | object |  |
| `lines[].description` | string |  |
| `lines[].duedate` | string |  |
| `lines[].id` | number |  |
| `lines[].invoiced` | number |  |
| `lines[].item.id` | number |  |
| `lines[].item.name` | string |  |
| `lines[].job` | object |  |
| `lines[].lineNumber` | number |  |
| `lines[].linkedTransaction` | object |  |
| `lines[].listPrice` | object |  |
| `lines[].lot` | object |  |
| `lines[].margin` | object |  |
| `lines[].percentdiscount` | object |  |
| `lines[].picked` | number |  |
| `lines[].produced` | number |  |
| `lines[].quantity` | number |  |
| `lines[].returned` | number |  |
| `lines[].serials` | object |  |
| `lines[].shipped` | number |  |
| `lines[].tax.taxable` | boolean |  |
| `lines[].tax.taxCode` | object |  |
| `lines[].tax.taxExemptReasonId` | object |  |
| `lines[].unitprice` | number |  |
| `lines[].uom` | object |  |
| `lines[].volume` | number |  |
| `lines[].volumeunit` | string |  |
| `lines[].weight` | number |  |
| `lines[].weightunit` | string |  |
| `lines[].workcenter` | object |  |
| `linkedTransaction` | object |  |
| `location.id` | number |  |
| `location.name` | string |  |
| `number` | string |  |
| `orderStage` | object |  |
| `priority` | object |  |
| `salesRep` | object |  |
| `serial` | object |  |
| `shipping.address.city` | object |  |
| `shipping.address.country` | object |  |
| `shipping.address.line1` | object |  |
| `shipping.address.line2` | object |  |
| `shipping.address.line3` | object |  |
| `shipping.address.line4` | object |  |
| `shipping.address.line5` | object |  |
| `shipping.address.postalCode` | object |  |
| `shipping.address.stateProvince` | object |  |
| `shipping.addressName` | string |  |
| `shipping.addressType` | string |  |
| `shipping.company` | object |  |
| `shipping.contact` | object |  |
| `shipping.email` | object |  |
| `shipping.phone` | object |  |
| `shippingAmount` | number |  |
| `shippingTaxable` | boolean |  |
| `starred` | number |  |
| `statusLink` | string |  |
| `statusMessage` | string |  |
| `storeCustomerToken` | boolean |  |
| `subTotal` | number |  |
| `summaryOnly` | boolean |  |
| `syncToken` | number |  |
| `taxAmount` | number |  |
| `taxCode` | object |  |
| `taxPercent` | number |  |
| `terms` | object |  |
| `total` | number |  |
| `transactionLocationQuickBooks` | string |  |
| `values` | object |  |

## Native endpoint

Through the native SOS Inventory API, this operation is `PUT /api/v2/salesorder/:id` (base URL `https://api.sosinventory.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-sales-order.md) for the provider-specific parameters and requirements.

