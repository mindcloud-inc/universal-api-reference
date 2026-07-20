# SOS Inventory: Update Purchase Order

Updates an existing purchase order in SOS Inventory.

```
PUT https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/update-purchase-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SOS Inventory `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/update-purchase-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "number": "string",
  "date": "string",
  "vendor.name": "Ava Chen",
  "location.name": "Ava Chen",
  "lines[].item.name": "Ava Chen",
  "lines[].quantity": 1,
  "lines[].unitPrice": 1,
  "lines[].amount": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/update-purchase-order', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "number": "string",
    "date": "string",
    "vendor.name": "Ava Chen",
    "location.name": "Ava Chen",
    "lines[].item.name": "Ava Chen",
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
| `id` | number | yes | Purchase order ID in the request path. |
| `syncToken` | number | no | Current record version from the latest GET response. |
| `number` | string | yes | Current purchase order number. |
| `date` | string | yes | Transaction date in YYYY-MM-DDTHH:MM:SS format. |
| `vendor.name` | string | yes | Vendor name. |
| `location.name` | string | yes | Location name. |
| `comment` | string | no | Internal company comment. |
| `lines[].item.name` | string | yes | Item name for the first purchase-order line. |
| `lines[].quantity` | number | yes | Quantity for the first purchase-order line. |
| `lines[].unitPrice` | number | yes | Per-unit purchase cost for the first line. |
| `lines[].amount` | number | yes | Line amount. Must equal quantity multiplied by unit price. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
      "blanketPO": true,
      "closed": true,
      "comment": "string",
      "confirmed": true,
      "contractManufacturing": true,
      "currency": {},
      "customer": {},
      "customFields": {},
      "date": "string",
      "deleted": true,
      "department": {},
      "depositAmount": 1,
      "dropShip": true,
      "exchangeRate": 1,
      "expectedDate": {},
      "expectedShip": {},
      "hasSignature": true,
      "id": 1,
      "keys": {},
      "lastSync": "string",
      "lines": [
        {
          "amount": 1,
          "bin": {},
          "class": {},
          "customer": {},
          "description": "string",
          "id": 1,
          "item": {
            "id": 1,
            "name": "Ava Chen"
          },
          "job": {},
          "lineNumber": 1,
          "linkedTransaction": {},
          "lot": {},
          "lotExpiration": {},
          "quantity": 1,
          "received": 1,
          "serials": {},
          "tax": {
            "taxable": true,
            "taxCode": {},
            "taxExemptReasonId": {}
          },
          "unitprice": 1,
          "uom": {},
          "vendorPartNumber": "string",
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
      "openAmount": 1,
      "pendingApproval": true,
      "receivedStatus": "string",
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
      "shippingMethod": {},
      "starred": 1,
      "subTotal": 1,
      "summaryOnly": true,
      "syncMessage": {},
      "syncToken": 1,
      "taxAmount": 1,
      "taxCode": {},
      "terms": {},
      "total": 1,
      "trackingNumber": "string",
      "updateDefaultCosts": true,
      "values": {},
      "vendor": {
        "id": 1,
        "name": "Ava Chen"
      },
      "vendorMessage": "string",
      "vendorNotes": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
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
| `blanketPO` | boolean |  |
| `closed` | boolean |  |
| `comment` | string |  |
| `confirmed` | boolean |  |
| `contractManufacturing` | boolean |  |
| `currency` | object |  |
| `customer` | object |  |
| `customFields` | object |  |
| `date` | string |  |
| `deleted` | boolean |  |
| `department` | object |  |
| `depositAmount` | number |  |
| `dropShip` | boolean |  |
| `exchangeRate` | number |  |
| `expectedDate` | object |  |
| `expectedShip` | object |  |
| `hasSignature` | boolean |  |
| `id` | number |  |
| `keys` | object |  |
| `lastSync` | string |  |
| `lines[].amount` | number |  |
| `lines[].bin` | object |  |
| `lines[].class` | object |  |
| `lines[].customer` | object |  |
| `lines[].description` | string |  |
| `lines[].id` | number |  |
| `lines[].item.id` | number |  |
| `lines[].item.name` | string |  |
| `lines[].job` | object |  |
| `lines[].lineNumber` | number |  |
| `lines[].linkedTransaction` | object |  |
| `lines[].lot` | object |  |
| `lines[].lotExpiration` | object |  |
| `lines[].quantity` | number |  |
| `lines[].received` | number |  |
| `lines[].serials` | object |  |
| `lines[].tax.taxable` | boolean |  |
| `lines[].tax.taxCode` | object |  |
| `lines[].tax.taxExemptReasonId` | object |  |
| `lines[].unitprice` | number |  |
| `lines[].uom` | object |  |
| `lines[].vendorPartNumber` | string |  |
| `lines[].volume` | number |  |
| `lines[].volumeunit` | string |  |
| `lines[].weight` | number |  |
| `lines[].weightunit` | string |  |
| `lines[].workcenter` | object |  |
| `linkedTransaction` | object |  |
| `location.id` | number |  |
| `location.name` | string |  |
| `number` | string |  |
| `openAmount` | number |  |
| `pendingApproval` | boolean |  |
| `receivedStatus` | string |  |
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
| `shippingMethod` | object |  |
| `starred` | number |  |
| `subTotal` | number |  |
| `summaryOnly` | boolean |  |
| `syncMessage` | object |  |
| `syncToken` | number |  |
| `taxAmount` | number |  |
| `taxCode` | object |  |
| `terms` | object |  |
| `total` | number |  |
| `trackingNumber` | string |  |
| `updateDefaultCosts` | boolean |  |
| `values` | object |  |
| `vendor.id` | number |  |
| `vendor.name` | string |  |
| `vendorMessage` | string |  |
| `vendorNotes` | string |  |

## Native endpoint

Through the native SOS Inventory API, this operation is `PUT /api/v2/purchaseorder/:id` (base URL `https://api.sosinventory.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-purchase-order.md) for the provider-specific parameters and requirements.

