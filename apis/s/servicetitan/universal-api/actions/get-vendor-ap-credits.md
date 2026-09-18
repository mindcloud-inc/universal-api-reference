# ServiceTitan: Get Vendor AP Credits

Retrieves vendor bills from ServiceTitan.

```
GET https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/get-vendor-ap-credits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceTitan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/get-vendor-ap-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/get-vendor-ap-credits?${params}`, {
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
| `ids` | string | no | Comma-separated list of specific AP credit IDs to retrieve Accepts multiple values in one string, delimited by `,`. |
| `page` | number | no | The logical page number to return, starting from 1 |
| `pageSize` | number | no | How many records to return (50 by default) |
| `createdBefore` | date | no | Return items created before certain date/time (in UTC) |
| `createdOnOrAfter` | date | no | Return items created on or after certain date/time (in UTC) |
| `modifiedBefore` | date | no | Return items modified before certain date/time (in UTC) |
| `modifiedOnOrAfter` | date | no | Return items modified on or after certain date/time (in UTC) |
| `sort` | string | no | Applies sorting by specified fields |
| `customField.Fields` | object | no | Dictionary of custom-field name-value pairs |
| `customField.Operator` | list<string> | no | Operator between custom-field name-value pairs. Values: And, Or; default: And. One of: `And`, `Or`. |
| `syncStatuses` | list<string> | no | Filter by sync status values One of: `Exported`, `Pending`, `Posted`, `PostedAndExported`. Accepts multiple values as an array. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `includeTotal` | boolean | no | Whether total count should be returned |

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

Through the native ServiceTitan API, this operation is `GET accounting/v2/tenant/{{credentials.tenant}}/ap-credits` (base URL `https://{{credentials.baseUrl}}/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-vendor-ap-credits.md) for the provider-specific parameters and requirements.

