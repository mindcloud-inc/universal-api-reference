# ServiceTitan: Mark Invoice as Exported

Update Invoice record.

```
PUT https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/mark-invoice-as-exported
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceTitan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/mark-invoice-as-exported" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/mark-invoice-as-exported', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `invoiceId` | number | no |  |
| `externalId` | string | no |  |
| `externalMessage` | string | no |  |
| `model` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "adjustmentToId": {},
      "assignedTo": {},
      "balance": "string",
      "batch": {
        "id": 1,
        "name": "Ava Chen",
        "number": "string"
      },
      "businessUnit": {
        "id": 1,
        "name": "Ava Chen"
      },
      "commissionEligibilityDate": {},
      "createdBy": "string",
      "createdOn": "string",
      "customer": {
        "id": 1,
        "name": "Ava Chen"
      },
      "customerAddress": {
        "city": "string",
        "country": "string",
        "state": "string",
        "street": "string",
        "unit": {},
        "zip": "string"
      },
      "customFields": {},
      "depositedOn": "string",
      "discountTotal": "string",
      "dueDate": "string",
      "employeeInfo": {
        "id": 1,
        "modifiedOn": "string",
        "name": "Ava Chen"
      },
      "exportId": "string",
      "id": 1,
      "importId": {},
      "invoiceDate": "string",
      "invoiceType": {},
      "items": [
        {
          "addOn": true,
          "assetAccount": {},
          "businessUnit": {
            "id": 1,
            "name": "Ava Chen"
          },
          "cost": "string",
          "costOfSaleAccount": {
            "detailType": "string",
            "id": 1,
            "name": "Ava Chen",
            "number": "string",
            "type": "string"
          },
          "createdById": 1,
          "createdOn": "string",
          "description": "string",
          "displayInAmount": true,
          "displayName": "Ava Chen",
          "estimateItemId": {},
          "exportId": {},
          "generalLedgerAccount": {
            "detailType": "string",
            "id": 1,
            "name": "Ava Chen",
            "number": "string",
            "type": "string"
          },
          "id": 1,
          "importId": {},
          "installedEquipmentId": {},
          "inventory": true,
          "inventoryLocation": {},
          "inventoryLocationId": {},
          "inventoryStatus": "string",
          "itemGroup": {},
          "memberPrice": "string",
          "membershipTypeId": 1,
          "modifiedOn": "string",
          "order": 1,
          "price": "string",
          "quantity": "string",
          "serviceDate": "string",
          "skuId": 1,
          "skuName": "Ava Chen",
          "soldHours": 1,
          "taxable": true,
          "technicianId": {},
          "total": "string",
          "totalCost": "string",
          "type": "string"
        }
      ],
      "job": {
        "id": 1,
        "number": "string",
        "type": "string"
      },
      "location": {
        "id": 1,
        "name": "Ava Chen"
      },
      "locationAddress": {
        "city": "string",
        "country": "string",
        "state": "string",
        "street": "string",
        "unit": "string",
        "zip": "string"
      },
      "materialSkuId": 1,
      "membershipId": {},
      "modifiedOn": "string",
      "paidOn": "string",
      "projectId": {},
      "referenceNumber": "string",
      "reviewStatus": "string",
      "royalty": {
        "date": {},
        "memo": {},
        "sentOn": {},
        "status": "string"
      },
      "salesTax": "string",
      "salesTaxCode": {
        "id": 1,
        "name": "Ava Chen",
        "taxRate": 1
      },
      "sentStatus": "string",
      "subTotal": "string",
      "summary": "string",
      "syncStatus": "string",
      "termName": "Ava Chen",
      "total": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `adjustmentToId` | object |  |
| `assignedTo` | object |  |
| `balance` | string |  |
| `batch.id` | number |  |
| `batch.name` | string |  |
| `batch.number` | string |  |
| `businessUnit.id` | number |  |
| `businessUnit.name` | string |  |
| `commissionEligibilityDate` | object |  |
| `createdBy` | string |  |
| `createdOn` | string |  |
| `customer.id` | number |  |
| `customer.name` | string |  |
| `customerAddress.city` | string |  |
| `customerAddress.country` | string |  |
| `customerAddress.state` | string |  |
| `customerAddress.street` | string |  |
| `customerAddress.unit` | object |  |
| `customerAddress.zip` | string |  |
| `customFields` | object |  |
| `depositedOn` | string |  |
| `discountTotal` | string |  |
| `dueDate` | string |  |
| `employeeInfo.id` | number |  |
| `employeeInfo.modifiedOn` | string |  |
| `employeeInfo.name` | string |  |
| `exportId` | string |  |
| `id` | number |  |
| `importId` | object |  |
| `invoiceDate` | string |  |
| `invoiceType` | object |  |
| `items[].addOn` | boolean |  |
| `items[].assetAccount` | object |  |
| `items[].businessUnit.id` | number |  |
| `items[].businessUnit.name` | string |  |
| `items[].cost` | string |  |
| `items[].costOfSaleAccount.detailType` | string |  |
| `items[].costOfSaleAccount.id` | number |  |
| `items[].costOfSaleAccount.name` | string |  |
| `items[].costOfSaleAccount.number` | string |  |
| `items[].costOfSaleAccount.type` | string |  |
| `items[].createdById` | number |  |
| `items[].createdOn` | string |  |
| `items[].description` | string |  |
| `items[].displayInAmount` | boolean |  |
| `items[].displayName` | string |  |
| `items[].estimateItemId` | object |  |
| `items[].exportId` | object |  |
| `items[].generalLedgerAccount.detailType` | string |  |
| `items[].generalLedgerAccount.id` | number |  |
| `items[].generalLedgerAccount.name` | string |  |
| `items[].generalLedgerAccount.number` | string |  |
| `items[].generalLedgerAccount.type` | string |  |
| `items[].id` | number |  |
| `items[].importId` | object |  |
| `items[].installedEquipmentId` | object |  |
| `items[].inventory` | boolean |  |
| `items[].inventoryLocation` | object |  |
| `items[].inventoryLocationId` | object |  |
| `items[].inventoryStatus` | string |  |
| `items[].itemGroup` | object |  |
| `items[].memberPrice` | string |  |
| `items[].membershipTypeId` | number |  |
| `items[].modifiedOn` | string |  |
| `items[].order` | number |  |
| `items[].price` | string |  |
| `items[].quantity` | string |  |
| `items[].serviceDate` | string |  |
| `items[].skuId` | number |  |
| `items[].skuName` | string |  |
| `items[].soldHours` | number |  |
| `items[].taxable` | boolean |  |
| `items[].technicianId` | object |  |
| `items[].total` | string |  |
| `items[].totalCost` | string |  |
| `items[].type` | string |  |
| `job.id` | number |  |
| `job.number` | string |  |
| `job.type` | string |  |
| `location.id` | number |  |
| `location.name` | string |  |
| `locationAddress.city` | string |  |
| `locationAddress.country` | string |  |
| `locationAddress.state` | string |  |
| `locationAddress.street` | string |  |
| `locationAddress.unit` | string |  |
| `locationAddress.zip` | string |  |
| `materialSkuId` | number |  |
| `membershipId` | object |  |
| `modifiedOn` | string |  |
| `paidOn` | string |  |
| `projectId` | object |  |
| `referenceNumber` | string |  |
| `reviewStatus` | string |  |
| `royalty.date` | object |  |
| `royalty.memo` | object |  |
| `royalty.sentOn` | object |  |
| `royalty.status` | string |  |
| `salesTax` | string |  |
| `salesTaxCode.id` | number |  |
| `salesTaxCode.name` | string |  |
| `salesTaxCode.taxRate` | number |  |
| `sentStatus` | string |  |
| `subTotal` | string |  |
| `summary` | string |  |
| `syncStatus` | string |  |
| `termName` | string |  |
| `total` | string |  |

## Native endpoint

Through the native ServiceTitan API, this operation is `POST accounting/v2/tenant/{{credentials.tenant}}/invoices/markasexported` (base URL `https://{{credentials.baseUrl}}/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/mark-invoice-as-exported.md) for the provider-specific parameters and requirements.

