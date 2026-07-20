# DateX (Legacy): Create Sales Order



```
POST https://connect.mindcloud.co/v1/universal/dateX/latest/actions/create-sales-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DateX (Legacy) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dateX/latest/actions/create-sales-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dateX/latest/actions/create-sales-order', {
  method: 'POST',
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
| `order.addresses[].type` | string | no |  |
| `order.customFields[].name` | string | no |  |
| `order.instructions[].instructionId` | number | no |  |
| `order.orderLines[].childLines[].customFields[].name` | string | no |  |
| `order.orderLines[].childLines[].lineNumber` | number | no |  |
| `order.orderLines[].customFields[].name` | string | no |  |
| `order.orderLines[].lineNumber` | number | no |  |
| `order.owner` | string | no |  |
| `order.shipments[].billOfLading` | string | no |  |
| `order.addresses[].name` | string | no |  |
| `order.customFields[].value` | string | no |  |
| `order.instructions[].isEnabled` | boolean | no |  |
| `order.orderLines[].childLines[].customFields[].value` | string | no |  |
| `order.orderLines[].childLines[].material` | string | no |  |
| `order.orderLines[].customFields[].value` | string | no |  |
| `order.orderLines[].material` | string | no |  |
| `order.project` | string | no |  |
| `order.shipments[].bookingNumber` | string | no |  |
| `order.addresses[].reference` | string | no |  |
| `order.instructions[].entityName` | string | no |  |
| `order.orderClass` | string | no |  |
| `order.orderLines[].childLines[].vendorLot` | string | no |  |
| `order.orderLines[].vendorLot` | string | no |  |
| `order.shipments[].lookup` | string | no |  |
| `order.addresses[].attentionOf` | string | no |  |
| `order.instructions[].entityKeys` | string | no |  |
| `order.orderLines[].childLines[].lot` | string | no |  |
| `order.orderLines[].lot` | string | no |  |
| `order.ownerReference` | string | no |  |
| `order.shipments[].expectedWarehouse` | string | no |  |
| `order.addresses[].line1` | string | no |  |
| `order.instructions[].type` | string | no |  |
| `order.orderLines[].childLines[].packaging` | string | no |  |
| `order.orderLines[].packaging` | string | no |  |
| `order.shipments[].backOrder` | boolean | no |  |
| `order.vendorReference` | string | no |  |
| `order.addresses[].line2` | string | no |  |
| `order.instructions[].createdOn` | string | no |  |
| `order.orderLines[].childLines[].packagedAmount` | number | no |  |
| `order.orderLines[].packagedAmount` | number | no |  |
| `order.requestedDeliveryDate` | string | no |  |
| `order.addresses[].city` | string | no |  |
| `order.instructions[].createdBy` | string | no |  |
| `order.orderLines[].childLines[].upc` | string | no |  |
| `order.orderLines[].upc` | string | no |  |
| `order.warehouse` | string | no |  |
| `order.addresses[].state` | string | no |  |
| `order.carrier` | string | no |  |
| `order.instructions[].modifiedOn` | string | no |  |
| `order.orderLines[].childLines[]` | array | no |  |
| `order.orderLines[].childLines[].customFields[]` | array<object> | no |  |
| `order.addresses[].postalCode` | string | no |  |
| `order.carrierService` | string | no |  |
| `order.instructions[].modifiedBy` | string | no |  |
| `order.orderLines[].childLines[].cost` | number | no |  |
| `order.orderLines[].customFields[]` | array | no |  |
| `order.addresses[]` | array<object> | no |  |
| `order.addresses[].country` | string | no |  |
| `order.instructions[].instruction` | string | no |  |
| `order.orderLines[].childLines[].price` | string | no |  |
| `order.orderLines[].orderId` | number | no |  |
| `order.addresses[].lookup` | string | no |  |
| `order.orderLines[]` | array<object> | no |  |
| `order.orderLines[].cost` | number | no |  |
| `order.addresses[].phone` | string | no |  |
| `order.customFields[]` | array<object> | no |  |
| `order.orderLines[].price` | number | no |  |
| `order.addresses[].email` | string | no |  |
| `order.shipments[]` | array<object> | no |  |
| `order.addresses[].fax` | string | no |  |
| `order.lookup` | string | no |  |
| `order.addresses[].title` | string | no |  |
| `order.instructions[]` | array<object> | no |  |
| `order.addresses[].greeting` | string | no |  |
| `order.currency` | string | no |  |
| `order.addresses[].firstName` | string | no |  |
| `order.notes` | string | no |  |
| `order.addresses[].middleName` | string | no |  |
| `order.projectId` | string | no |  |
| `order` | object | no |  |
| `order.addresses[].lastName` | string | no |  |
| `order.addresses[].isResidential` | boolean | no |  |
| `order.addresses[].notes` | string | no |  |
| `order.addresses[].orderId` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addresses": [
        {
          "attentionOf": {},
          "city": "string",
          "country": "string",
          "email": {},
          "fax": {},
          "firstName": "Ava",
          "greeting": {},
          "isResidential": {},
          "lastName": "Chen",
          "line1": "string",
          "line2": {},
          "line3": {},
          "line4": {},
          "lookup": {},
          "middleName": {},
          "name": "Ava Chen",
          "notes": {},
          "orderAddressId": 1,
          "orderId": 1,
          "phone": {},
          "postalCode": "string",
          "reference": {},
          "state": "string",
          "title": {},
          "type": "string"
        }
      ],
      "carrier": "string",
      "createdOn": "string",
      "fulfilledOn": "string",
      "lookup": "string",
      "modifiedBy": "string",
      "modifiedOn": "string",
      "notes": {},
      "orderClass": "string",
      "orderId": 1,
      "orderLines": [
        {
          "childLines": {},
          "cost": {},
          "customFields": {},
          "grossWeight": {},
          "licensePlate": {},
          "lineNumber": 1,
          "lot": "string",
          "material": "string",
          "netWeight": {},
          "notes": {},
          "orderId": {},
          "packagedAmount": 1,
          "packaging": {},
          "parentLineNumber": {},
          "price": {},
          "serialNumber": {},
          "shipment": {},
          "shippedContents": [
            {
              "baseAmount": 1,
              "grossWeight": 1,
              "material": "string",
              "netWeight": 1,
              "packagedAmount": 1,
              "packaging": "string",
              "serialNumbers": {},
              "weightUom": "string"
            }
          ],
          "status": "string",
          "upc": {},
          "vendorLot": "string",
          "weightUom": {}
        }
      ],
      "owner": "string",
      "ownerReference": "string",
      "project": "string",
      "requestedDeliveryDate": {},
      "shipments": [
        {
          "actualWarehouse": "string",
          "availableDate": {},
          "backOrder": true,
          "billOfLading": "string",
          "carrier": "string",
          "carrierService": "string",
          "expectedDate": {},
          "expectedWarehouse": "string",
          "lookup": "string",
          "notes": "string",
          "pickupDate": "string",
          "shipmentId": 1,
          "trackingIdentifier": "string"
        }
      ],
      "shippedContents": [
        {
          "baseAmount": 1,
          "grossWeight": 1,
          "material": "string",
          "netWeight": 1,
          "packagedAmount": 1,
          "packaging": "string",
          "serialNumbers": {},
          "weightUom": "string"
        }
      ],
      "shippingInfo": [
        {
          "shipment": {
            "lookup": "string",
            "shipmentId": 1,
            "status": "string"
          },
          "shippingContainers": [
            {
              "billOfLading": {},
              "bondNumber": {},
              "commodityDescription": {},
              "containerNumber": {},
              "customsReleaseNumber": {},
              "declaredValue": {},
              "estimatedDeliveryDate": {},
              "height": {},
              "length": {},
              "licensePlates": [
                {
                  "licensePlateId": 1,
                  "lookup": "string",
                  "serialNumbers": {}
                }
              ],
              "lookup": "string",
              "manifestedPackageBundleCode": {},
              "manifestedPackageCode": {},
              "nmfcNumber": {},
              "nmfcSubNumber": {},
              "notes": {},
              "packagedItemCount": {},
              "parentId": {},
              "sailOnBoard": {},
              "sealId": {},
              "shippingContainerId": 1,
              "shippingCost": {},
              "shippingDate": {},
              "trackingNumber": "string",
              "trailerNumber": {},
              "volume": {},
              "weight": 1,
              "width": {}
            }
          ]
        }
      ],
      "status": "string",
      "tasks": [
        {
          "material": "string",
          "notes": "string",
          "operationCode": "string",
          "orderLineNumber": 1,
          "status": "string",
          "taskId": 1
        }
      ],
      "vendorReference": "string",
      "warehouse": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addresses[].attentionOf` | object |  |
| `addresses[].city` | string |  |
| `addresses[].country` | string |  |
| `addresses[].email` | object |  |
| `addresses[].fax` | object |  |
| `addresses[].firstName` | string |  |
| `addresses[].greeting` | object |  |
| `addresses[].isResidential` | object |  |
| `addresses[].lastName` | string |  |
| `addresses[].line1` | string |  |
| `addresses[].line2` | object |  |
| `addresses[].line3` | object |  |
| `addresses[].line4` | object |  |
| `addresses[].lookup` | object |  |
| `addresses[].middleName` | object |  |
| `addresses[].name` | string |  |
| `addresses[].notes` | object |  |
| `addresses[].orderAddressId` | number |  |
| `addresses[].orderId` | number |  |
| `addresses[].phone` | object |  |
| `addresses[].postalCode` | string |  |
| `addresses[].reference` | object |  |
| `addresses[].state` | string |  |
| `addresses[].title` | object |  |
| `addresses[].type` | string |  |
| `carrier` | string |  |
| `createdOn` | string |  |
| `fulfilledOn` | string |  |
| `lookup` | string |  |
| `modifiedBy` | string |  |
| `modifiedOn` | string |  |
| `notes` | object |  |
| `orderClass` | string |  |
| `orderId` | number |  |
| `orderLines[].childLines` | object |  |
| `orderLines[].cost` | object |  |
| `orderLines[].customFields` | object |  |
| `orderLines[].grossWeight` | object |  |
| `orderLines[].licensePlate` | object |  |
| `orderLines[].lineNumber` | number |  |
| `orderLines[].lot` | string |  |
| `orderLines[].material` | string |  |
| `orderLines[].netWeight` | object |  |
| `orderLines[].notes` | object |  |
| `orderLines[].orderId` | object |  |
| `orderLines[].packagedAmount` | number |  |
| `orderLines[].packaging` | object |  |
| `orderLines[].parentLineNumber` | object |  |
| `orderLines[].price` | object |  |
| `orderLines[].serialNumber` | object |  |
| `orderLines[].shipment` | object |  |
| `orderLines[].shippedContents[].baseAmount` | number |  |
| `orderLines[].shippedContents[].grossWeight` | number |  |
| `orderLines[].shippedContents[].material` | string |  |
| `orderLines[].shippedContents[].netWeight` | number |  |
| `orderLines[].shippedContents[].packagedAmount` | number |  |
| `orderLines[].shippedContents[].packaging` | string |  |
| `orderLines[].shippedContents[].serialNumbers` | object |  |
| `orderLines[].shippedContents[].weightUom` | string |  |
| `orderLines[].status` | string |  |
| `orderLines[].upc` | object |  |
| `orderLines[].vendorLot` | string |  |
| `orderLines[].weightUom` | object |  |
| `owner` | string |  |
| `ownerReference` | string |  |
| `project` | string |  |
| `requestedDeliveryDate` | object |  |
| `shipments[].actualWarehouse` | string |  |
| `shipments[].availableDate` | object |  |
| `shipments[].backOrder` | boolean |  |
| `shipments[].billOfLading` | string |  |
| `shipments[].carrier` | string |  |
| `shipments[].carrierService` | string |  |
| `shipments[].expectedDate` | object |  |
| `shipments[].expectedWarehouse` | string |  |
| `shipments[].lookup` | string |  |
| `shipments[].notes` | string |  |
| `shipments[].pickupDate` | string |  |
| `shipments[].shipmentId` | number |  |
| `shipments[].trackingIdentifier` | string |  |
| `shippedContents[].baseAmount` | number |  |
| `shippedContents[].grossWeight` | number |  |
| `shippedContents[].material` | string |  |
| `shippedContents[].netWeight` | number |  |
| `shippedContents[].packagedAmount` | number |  |
| `shippedContents[].packaging` | string |  |
| `shippedContents[].serialNumbers` | object |  |
| `shippedContents[].weightUom` | string |  |
| `shippingInfo[].shipment.lookup` | string |  |
| `shippingInfo[].shipment.shipmentId` | number |  |
| `shippingInfo[].shipment.status` | string |  |
| `shippingInfo[].shippingContainers[].billOfLading` | object |  |
| `shippingInfo[].shippingContainers[].bondNumber` | object |  |
| `shippingInfo[].shippingContainers[].commodityDescription` | object |  |
| `shippingInfo[].shippingContainers[].containerNumber` | object |  |
| `shippingInfo[].shippingContainers[].customsReleaseNumber` | object |  |
| `shippingInfo[].shippingContainers[].declaredValue` | object |  |
| `shippingInfo[].shippingContainers[].estimatedDeliveryDate` | object |  |
| `shippingInfo[].shippingContainers[].height` | object |  |
| `shippingInfo[].shippingContainers[].length` | object |  |
| `shippingInfo[].shippingContainers[].licensePlates[].licensePlateId` | number |  |
| `shippingInfo[].shippingContainers[].licensePlates[].lookup` | string |  |
| `shippingInfo[].shippingContainers[].licensePlates[].serialNumbers` | object |  |
| `shippingInfo[].shippingContainers[].lookup` | string |  |
| `shippingInfo[].shippingContainers[].manifestedPackageBundleCode` | object |  |
| `shippingInfo[].shippingContainers[].manifestedPackageCode` | object |  |
| `shippingInfo[].shippingContainers[].nmfcNumber` | object |  |
| `shippingInfo[].shippingContainers[].nmfcSubNumber` | object |  |
| `shippingInfo[].shippingContainers[].notes` | object |  |
| `shippingInfo[].shippingContainers[].packagedItemCount` | object |  |
| `shippingInfo[].shippingContainers[].parentId` | object |  |
| `shippingInfo[].shippingContainers[].sailOnBoard` | object |  |
| `shippingInfo[].shippingContainers[].sealId` | object |  |
| `shippingInfo[].shippingContainers[].shippingContainerId` | number |  |
| `shippingInfo[].shippingContainers[].shippingCost` | object |  |
| `shippingInfo[].shippingContainers[].shippingDate` | object |  |
| `shippingInfo[].shippingContainers[].trackingNumber` | string |  |
| `shippingInfo[].shippingContainers[].trailerNumber` | object |  |
| `shippingInfo[].shippingContainers[].volume` | object |  |
| `shippingInfo[].shippingContainers[].weight` | number |  |
| `shippingInfo[].shippingContainers[].width` | object |  |
| `status` | string |  |
| `tasks[].material` | string |  |
| `tasks[].notes` | string |  |
| `tasks[].operationCode` | string |  |
| `tasks[].orderLineNumber` | number |  |
| `tasks[].status` | string |  |
| `tasks[].taskId` | number |  |
| `vendorReference` | string |  |
| `warehouse` | string |  |

## Native endpoint

Through the native DateX (Legacy) API, this operation is `POST sales_orders/create` (base URL `https://{{credentials.environment}}.wavelength.host/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sales-order.md) for the provider-specific parameters and requirements.

