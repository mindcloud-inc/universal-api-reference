# DateX (Legacy) Universal API Examples

These examples use the MindCloud API key and DateX (Legacy) connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Echo Test



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dateX/latest/actions/echo-test?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dateX/latest/actions/echo-test?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "greeting": "string"
    }
  ],
  "meta": {}
}
```

See the full [Echo Test action reference](actions/echo-test.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dateX/latest/actions/echo-test).

## Create Sales Order



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

Example response:

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

See the full [Create Sales Order action reference](actions/create-sales-order.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dateX/latest/actions/create-sales-order).
