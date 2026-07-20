# Logiwa Legacy WMS: List Purchase Orders

By using this endpoint, the users can obtain the list of all the purchase orders based on the entered criteria.

```
GET https://connect.mindcloud.co/v1/universal/logiwaLegacyWMS/latest/actions/list-purchase-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Logiwa Legacy WMS `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/logiwaLegacyWMS/latest/actions/list-purchase-orders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/logiwaLegacyWMS/latest/actions/list-purchase-orders?${params}`, {
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
| `code` | string | no | Purchase order code |

## Response

```json
{
  "success": true,
  "data": [
    {
      "approvalTemplateDescription": "string",
      "approvalTemplateID": {},
      "channelCode": "string",
      "code": "string",
      "confirmationDate": "string",
      "cutOffDate": "string",
      "deliveryTermsDescription": {},
      "deliveryTermsID": {},
      "departmentDescription": "string",
      "departmentID": {},
      "depositorCode": "string",
      "depositorDescription": "string",
      "depositorID": 1,
      "enteredBy": "string",
      "entryDateTime": "string",
      "entryDateTimeEnd": {},
      "entryDateTimeStart": {},
      "id": 1,
      "integrationKey": "string",
      "inventorySiteDescription": "string",
      "inventorySiteID": 1,
      "isExcelExport": true,
      "isProjectReturnClosed": {},
      "lastModifiedDate": "string",
      "lastModifiedDateEnd": {},
      "lastModifiedDateStart": {},
      "materialGroupDesc": "string",
      "notes": "string",
      "notes2": "string",
      "notes3": "string",
      "orderDate": "string",
      "orderDateEnd": {},
      "orderDateStart": {},
      "pageCount": 1,
      "pageSize": 1,
      "priority": "string",
      "projectDescription": {},
      "projectID": {},
      "purchaseAmount": {},
      "purchaseOrderItemList": {},
      "purchaseOrderStatusDescription": "string",
      "purchaseOrderStatusID": 1,
      "purchaseOrderTypeDescription": "string",
      "purchaseOrderTypeID": 1,
      "quarentineReasonDescription": {},
      "quarentineReasonID": {},
      "quotationDocs": "string",
      "recordCount": 1,
      "reqDeliveryDate": "string",
      "reqDeliveryDateEnd": {},
      "reqDeliveryDateStart": {},
      "schlineDate": "string",
      "selectedPageIndex": 1,
      "sODate": "string",
      "success": true,
      "successMessage": {},
      "suitabilityReasonDesc": {},
      "suitabilityReasonID": {},
      "supplierAddressDescription": "string",
      "supplierAddressID": 1,
      "supplierDescription": "string",
      "supplierID": 1,
      "supplierPartyID": 1,
      "warehouseDescription": "string",
      "warehouseID": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `approvalTemplateDescription` | string |  |
| `approvalTemplateID` | object |  |
| `channelCode` | string |  |
| `code` | string |  |
| `confirmationDate` | string |  |
| `cutOffDate` | string |  |
| `deliveryTermsDescription` | object |  |
| `deliveryTermsID` | object |  |
| `departmentDescription` | string |  |
| `departmentID` | object |  |
| `depositorCode` | string |  |
| `depositorDescription` | string |  |
| `depositorID` | number |  |
| `enteredBy` | string |  |
| `entryDateTime` | string |  |
| `entryDateTimeEnd` | object |  |
| `entryDateTimeStart` | object |  |
| `id` | number |  |
| `integrationKey` | string |  |
| `inventorySiteDescription` | string |  |
| `inventorySiteID` | number |  |
| `isExcelExport` | boolean |  |
| `isProjectReturnClosed` | object |  |
| `lastModifiedDate` | string |  |
| `lastModifiedDateEnd` | object |  |
| `lastModifiedDateStart` | object |  |
| `materialGroupDesc` | string |  |
| `notes` | string |  |
| `notes2` | string |  |
| `notes3` | string |  |
| `orderDate` | string |  |
| `orderDateEnd` | object |  |
| `orderDateStart` | object |  |
| `pageCount` | number |  |
| `pageSize` | number |  |
| `priority` | string |  |
| `projectDescription` | object |  |
| `projectID` | object |  |
| `purchaseAmount` | object |  |
| `purchaseOrderItemList` | object |  |
| `purchaseOrderStatusDescription` | string |  |
| `purchaseOrderStatusID` | number |  |
| `purchaseOrderTypeDescription` | string |  |
| `purchaseOrderTypeID` | number |  |
| `quarentineReasonDescription` | object |  |
| `quarentineReasonID` | object |  |
| `quotationDocs` | string |  |
| `recordCount` | number |  |
| `reqDeliveryDate` | string |  |
| `reqDeliveryDateEnd` | object |  |
| `reqDeliveryDateStart` | object |  |
| `schlineDate` | string |  |
| `selectedPageIndex` | number |  |
| `sODate` | string |  |
| `success` | boolean |  |
| `successMessage` | object |  |
| `suitabilityReasonDesc` | object |  |
| `suitabilityReasonID` | object |  |
| `supplierAddressDescription` | string |  |
| `supplierAddressID` | number |  |
| `supplierDescription` | string |  |
| `supplierID` | number |  |
| `supplierPartyID` | number |  |
| `warehouseDescription` | string |  |
| `warehouseID` | object |  |

## Native endpoint

Through the native Logiwa Legacy WMS API, this operation is `POST en/api/IntegrationApi/PurchaseOrderSearch` (base URL `https://{{credentials.uRL}}.logiwa.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-purchase-orders.md) for the provider-specific parameters and requirements.

