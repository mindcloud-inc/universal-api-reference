# Cin7 Core: Get Sale Attachment



```
GET https://connect.mindcloud.co/v1/universal/cin7core/latest/actions/get-sale-attachments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cin7 Core `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cin7core/latest/actions/get-sale-attachments?connectionId=$CONNECTION_ID&SaleID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "SaleID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cin7core/latest/actions/get-sale-attachments?${params}`, {
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
| `SaleID` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "additionalAttributes": {
        "additionalAttribute1": "string",
        "additionalAttribute10": "string",
        "additionalAttribute2": "string",
        "additionalAttribute3": "string",
        "additionalAttribute4": "string",
        "additionalAttribute5": "string",
        "additionalAttribute6": "string",
        "additionalAttribute7": "string",
        "additionalAttribute8": "string",
        "additionalAttribute9": "string"
      },
      "baseCurrency": "string",
      "billingAddress": {
        "city": "string",
        "country": "string",
        "displayAddressLine1": "string",
        "displayAddressLine2": "string",
        "line1": "string",
        "line2": "string",
        "postcode": "string",
        "state": "string"
      },
      "carrier": "string",
      "cOGSAmount": 1,
      "combinedInvoiceStatus": "string",
      "combinedPackingStatus": "string",
      "combinedPaymentStatus": "string",
      "combinedPickingStatus": "string",
      "combinedShippingStatus": "string",
      "combinedTrackingNumbers": "string",
      "contact": "string",
      "creditNotes": [
        {
          "creditNoteConversionRate": 1,
          "creditNoteDate": {},
          "creditNoteInvoiceNumber": "string",
          "creditNoteNumber": {},
          "memo": "string",
          "restockStatus": "string",
          "status": "string",
          "taskID": "string",
          "tax": 1,
          "total": 1,
          "totalBeforeTax": 1
        }
      ],
      "currencyRate": 1,
      "customer": "string",
      "customerCurrency": "string",
      "customerID": "string",
      "customerReference": "string",
      "defaultAccount": "string",
      "email": "ava@example.com",
      "externalID": "string",
      "fulfilments": [
        {
          "fulfillmentNumber": 1,
          "fulFilmentStatus": "string",
          "linkedInvoiceNumber": {},
          "pack": {
            "lines": [
              {
                "batchSN": {},
                "box": "string",
                "dimensionsUnits": "string",
                "expiryDate": {},
                "location": "string",
                "locationID": "string",
                "name": "Ava Chen",
                "nonInventory": true,
                "productCustomField1": "string",
                "productCustomField10": "string",
                "productCustomField2": "string",
                "productCustomField3": "string",
                "productCustomField4": "string",
                "productCustomField5": "string",
                "productCustomField6": "string",
                "productCustomField7": "string",
                "productCustomField8": "string",
                "productCustomField9": "string",
                "productHeight": 1,
                "productID": "string",
                "productLength": 1,
                "productWeight": 1,
                "productWidth": 1,
                "quantity": 1,
                "sku": "string",
                "weightUnits": "string"
              }
            ],
            "status": "string"
          },
          "pick": {
            "lines": [
              {
                "batchSN": {},
                "dimensionsUnits": "string",
                "expiryDate": {},
                "location": "string",
                "locationID": "string",
                "name": "Ava Chen",
                "nonInventory": true,
                "productCustomField1": "string",
                "productCustomField10": "string",
                "productCustomField2": "string",
                "productCustomField3": "string",
                "productCustomField4": "string",
                "productCustomField5": "string",
                "productCustomField6": "string",
                "productCustomField7": "string",
                "productCustomField8": "string",
                "productCustomField9": "string",
                "productHeight": 1,
                "productID": "string",
                "productLength": 1,
                "productWeight": 1,
                "productWidth": 1,
                "quantity": 1,
                "restockDate": {},
                "restockLocationID": {},
                "sku": "string",
                "weightUnits": "string"
              }
            ],
            "status": "string"
          },
          "ship": {
            "lines": [
              {
                "boxes": "string",
                "carrier": "string",
                "id": "string",
                "isShipped": true,
                "shipmentDate": "string",
                "trackingNumber": "string",
                "trackingURL": "https://example.com"
              }
            ],
            "requireBy": "string",
            "shippingAddress": {
              "city": "string",
              "company": "string",
              "contact": "string",
              "country": "string",
              "displayAddressLine1": "string",
              "displayAddressLine2": "string",
              "line1": "string",
              "line2": "string",
              "postcode": "string",
              "shipToOther": true,
              "state": "string"
            },
            "shippingNotes": "string",
            "status": "string"
          },
          "taskID": "string"
        }
      ],
      "fulFilmentStatus": "string",
      "id": "string",
      "inventoryMovements": [
        {
          "cogs": 1,
          "date": "string",
          "dimensionsUnits": "string",
          "productCustomField1": "string",
          "productCustomField10": "string",
          "productCustomField2": "string",
          "productCustomField3": "string",
          "productCustomField4": "string",
          "productCustomField5": "string",
          "productCustomField6": "string",
          "productCustomField7": "string",
          "productCustomField8": "string",
          "productCustomField9": "string",
          "productHeight": 1,
          "productID": "string",
          "productLength": 1,
          "productWeight": 1,
          "productWidth": 1,
          "taskID": "string",
          "weightUnits": "string"
        }
      ],
      "invoices": [
        {
          "additionalCharges": [
            {
              "account": "string",
              "comment": {},
              "description": "string",
              "discount": 1,
              "price": 1,
              "quantity": 1,
              "tax": 1,
              "taxRule": "string",
              "total": 1
            }
          ],
          "billingAddressLine1": "string",
          "billingAddressLine2": "string",
          "currencyConversionRate": 1,
          "invoiceDate": "string",
          "invoiceDueDate": "string",
          "invoiceNumber": "string",
          "lines": [
            {
              "account": "string",
              "averageCost": 1,
              "comment": "string",
              "dimensionsUnits": "string",
              "discount": 1,
              "name": "Ava Chen",
              "price": 1,
              "productCustomField1": "string",
              "productCustomField10": "string",
              "productCustomField2": "string",
              "productCustomField3": "string",
              "productCustomField4": "string",
              "productCustomField5": "string",
              "productCustomField6": "string",
              "productCustomField7": "string",
              "productCustomField8": "string",
              "productCustomField9": "string",
              "productHeight": 1,
              "productID": "string",
              "productLength": 1,
              "productWeight": 1,
              "productWidth": 1,
              "quantity": 1,
              "sku": "string",
              "tax": 1,
              "taxRule": "string",
              "total": 1,
              "weightUnits": "string"
            }
          ],
          "linkedFulfillmentNumber": {},
          "memo": "string",
          "paid": 1,
          "payments": [
            {
              "account": "string",
              "amount": 1,
              "currencyRate": 1,
              "dateCreated": "string",
              "datePaid": "string",
              "id": "string",
              "reference": "string"
            }
          ],
          "status": "string",
          "taskID": "string",
          "tax": 1,
          "total": 1,
          "totalBeforeTax": 1
        }
      ],
      "lastModifiedOn": "string",
      "location": "string",
      "manualJournals": {
        "status": "string"
      },
      "note": "string",
      "order": {
        "additionalCharges": [
          {
            "comment": {},
            "description": "string",
            "discount": 1,
            "price": 1,
            "quantity": 1,
            "tax": 1,
            "taxRule": "string",
            "total": 1
          }
        ],
        "lines": [
          {
            "averageCost": 1,
            "backorderQuantity": 1,
            "comment": {},
            "dimensionsUnits": "string",
            "discount": 1,
            "dropShip": true,
            "name": "Ava Chen",
            "price": 1,
            "productCustomField1": "string",
            "productCustomField10": "string",
            "productCustomField2": "string",
            "productCustomField3": "string",
            "productCustomField4": "string",
            "productCustomField5": "string",
            "productCustomField6": "string",
            "productCustomField7": "string",
            "productCustomField8": "string",
            "productCustomField9": "string",
            "productHeight": 1,
            "productID": "string",
            "productLength": 1,
            "productWeight": 1,
            "productWidth": 1,
            "quantity": 1,
            "sku": "string",
            "tax": 1,
            "taxRule": "string",
            "total": 1,
            "weightUnits": "string"
          }
        ],
        "memo": "string",
        "saleOrderNumber": "string",
        "status": "string",
        "tax": 1,
        "total": 1,
        "totalBeforeTax": 1
      },
      "phone": "string",
      "priceTier": "string",
      "quote": {
        "memo": "string",
        "status": "string",
        "tax": 1,
        "total": 1,
        "totalBeforeTax": 1
      },
      "saleOrderDate": "string",
      "salesRepresentative": "string",
      "serviceOnly": true,
      "shipBy": "string",
      "shippingAddress": {
        "city": "string",
        "company": "string",
        "contact": "string",
        "country": "string",
        "displayAddressLine1": "string",
        "displayAddressLine2": "string",
        "id": {},
        "line1": "string",
        "line2": "string",
        "postcode": "string",
        "shipToOther": true,
        "state": "string"
      },
      "shippingNotes": "string",
      "skipQuote": true,
      "sourceChannel": "string",
      "status": "string",
      "taxCalculation": "string",
      "taxRule": "string",
      "terms": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `additionalAttributes.additionalAttribute1` | string |  |
| `additionalAttributes.additionalAttribute10` | string |  |
| `additionalAttributes.additionalAttribute2` | string |  |
| `additionalAttributes.additionalAttribute3` | string |  |
| `additionalAttributes.additionalAttribute4` | string |  |
| `additionalAttributes.additionalAttribute5` | string |  |
| `additionalAttributes.additionalAttribute6` | string |  |
| `additionalAttributes.additionalAttribute7` | string |  |
| `additionalAttributes.additionalAttribute8` | string |  |
| `additionalAttributes.additionalAttribute9` | string |  |
| `baseCurrency` | string |  |
| `billingAddress.city` | string |  |
| `billingAddress.country` | string |  |
| `billingAddress.displayAddressLine1` | string |  |
| `billingAddress.displayAddressLine2` | string |  |
| `billingAddress.line1` | string |  |
| `billingAddress.line2` | string |  |
| `billingAddress.postcode` | string |  |
| `billingAddress.state` | string |  |
| `carrier` | string |  |
| `cOGSAmount` | number |  |
| `combinedInvoiceStatus` | string |  |
| `combinedPackingStatus` | string |  |
| `combinedPaymentStatus` | string |  |
| `combinedPickingStatus` | string |  |
| `combinedShippingStatus` | string |  |
| `combinedTrackingNumbers` | string |  |
| `contact` | string |  |
| `creditNotes[].creditNoteConversionRate` | number |  |
| `creditNotes[].creditNoteDate` | object |  |
| `creditNotes[].creditNoteInvoiceNumber` | string |  |
| `creditNotes[].creditNoteNumber` | object |  |
| `creditNotes[].memo` | string |  |
| `creditNotes[].restockStatus` | string |  |
| `creditNotes[].status` | string |  |
| `creditNotes[].taskID` | string |  |
| `creditNotes[].tax` | number |  |
| `creditNotes[].total` | number |  |
| `creditNotes[].totalBeforeTax` | number |  |
| `currencyRate` | number |  |
| `customer` | string |  |
| `customerCurrency` | string |  |
| `customerID` | string |  |
| `customerReference` | string |  |
| `defaultAccount` | string |  |
| `email` | string |  |
| `externalID` | string |  |
| `fulfilments[].fulfillmentNumber` | number |  |
| `fulfilments[].fulFilmentStatus` | string |  |
| `fulfilments[].linkedInvoiceNumber` | object |  |
| `fulfilments[].pack.lines[].batchSN` | object |  |
| `fulfilments[].pack.lines[].box` | string |  |
| `fulfilments[].pack.lines[].dimensionsUnits` | string |  |
| `fulfilments[].pack.lines[].expiryDate` | object |  |
| `fulfilments[].pack.lines[].location` | string |  |
| `fulfilments[].pack.lines[].locationID` | string |  |
| `fulfilments[].pack.lines[].name` | string |  |
| `fulfilments[].pack.lines[].nonInventory` | boolean |  |
| `fulfilments[].pack.lines[].productCustomField1` | string |  |
| `fulfilments[].pack.lines[].productCustomField10` | string |  |
| `fulfilments[].pack.lines[].productCustomField2` | string |  |
| `fulfilments[].pack.lines[].productCustomField3` | string |  |
| `fulfilments[].pack.lines[].productCustomField4` | string |  |
| `fulfilments[].pack.lines[].productCustomField5` | string |  |
| `fulfilments[].pack.lines[].productCustomField6` | string |  |
| `fulfilments[].pack.lines[].productCustomField7` | string |  |
| `fulfilments[].pack.lines[].productCustomField8` | string |  |
| `fulfilments[].pack.lines[].productCustomField9` | string |  |
| `fulfilments[].pack.lines[].productHeight` | number |  |
| `fulfilments[].pack.lines[].productID` | string |  |
| `fulfilments[].pack.lines[].productLength` | number |  |
| `fulfilments[].pack.lines[].productWeight` | number |  |
| `fulfilments[].pack.lines[].productWidth` | number |  |
| `fulfilments[].pack.lines[].quantity` | number |  |
| `fulfilments[].pack.lines[].sku` | string |  |
| `fulfilments[].pack.lines[].weightUnits` | string |  |
| `fulfilments[].pack.status` | string |  |
| `fulfilments[].pick.lines[].batchSN` | object |  |
| `fulfilments[].pick.lines[].dimensionsUnits` | string |  |
| `fulfilments[].pick.lines[].expiryDate` | object |  |
| `fulfilments[].pick.lines[].location` | string |  |
| `fulfilments[].pick.lines[].locationID` | string |  |
| `fulfilments[].pick.lines[].name` | string |  |
| `fulfilments[].pick.lines[].nonInventory` | boolean |  |
| `fulfilments[].pick.lines[].productCustomField1` | string |  |
| `fulfilments[].pick.lines[].productCustomField10` | string |  |
| `fulfilments[].pick.lines[].productCustomField2` | string |  |
| `fulfilments[].pick.lines[].productCustomField3` | string |  |
| `fulfilments[].pick.lines[].productCustomField4` | string |  |
| `fulfilments[].pick.lines[].productCustomField5` | string |  |
| `fulfilments[].pick.lines[].productCustomField6` | string |  |
| `fulfilments[].pick.lines[].productCustomField7` | string |  |
| `fulfilments[].pick.lines[].productCustomField8` | string |  |
| `fulfilments[].pick.lines[].productCustomField9` | string |  |
| `fulfilments[].pick.lines[].productHeight` | number |  |
| `fulfilments[].pick.lines[].productID` | string |  |
| `fulfilments[].pick.lines[].productLength` | number |  |
| `fulfilments[].pick.lines[].productWeight` | number |  |
| `fulfilments[].pick.lines[].productWidth` | number |  |
| `fulfilments[].pick.lines[].quantity` | number |  |
| `fulfilments[].pick.lines[].restockDate` | object |  |
| `fulfilments[].pick.lines[].restockLocationID` | object |  |
| `fulfilments[].pick.lines[].sku` | string |  |
| `fulfilments[].pick.lines[].weightUnits` | string |  |
| `fulfilments[].pick.status` | string |  |
| `fulfilments[].ship.lines[].boxes` | string |  |
| `fulfilments[].ship.lines[].carrier` | string |  |
| `fulfilments[].ship.lines[].id` | string |  |
| `fulfilments[].ship.lines[].isShipped` | boolean |  |
| `fulfilments[].ship.lines[].shipmentDate` | string |  |
| `fulfilments[].ship.lines[].trackingNumber` | string |  |
| `fulfilments[].ship.lines[].trackingURL` | string |  |
| `fulfilments[].ship.requireBy` | string |  |
| `fulfilments[].ship.shippingAddress.city` | string |  |
| `fulfilments[].ship.shippingAddress.company` | string |  |
| `fulfilments[].ship.shippingAddress.contact` | string |  |
| `fulfilments[].ship.shippingAddress.country` | string |  |
| `fulfilments[].ship.shippingAddress.displayAddressLine1` | string |  |
| `fulfilments[].ship.shippingAddress.displayAddressLine2` | string |  |
| `fulfilments[].ship.shippingAddress.line1` | string |  |
| `fulfilments[].ship.shippingAddress.line2` | string |  |
| `fulfilments[].ship.shippingAddress.postcode` | string |  |
| `fulfilments[].ship.shippingAddress.shipToOther` | boolean |  |
| `fulfilments[].ship.shippingAddress.state` | string |  |
| `fulfilments[].ship.shippingNotes` | string |  |
| `fulfilments[].ship.status` | string |  |
| `fulfilments[].taskID` | string |  |
| `fulFilmentStatus` | string |  |
| `id` | string |  |
| `inventoryMovements[].cogs` | number |  |
| `inventoryMovements[].date` | string |  |
| `inventoryMovements[].dimensionsUnits` | string |  |
| `inventoryMovements[].productCustomField1` | string |  |
| `inventoryMovements[].productCustomField10` | string |  |
| `inventoryMovements[].productCustomField2` | string |  |
| `inventoryMovements[].productCustomField3` | string |  |
| `inventoryMovements[].productCustomField4` | string |  |
| `inventoryMovements[].productCustomField5` | string |  |
| `inventoryMovements[].productCustomField6` | string |  |
| `inventoryMovements[].productCustomField7` | string |  |
| `inventoryMovements[].productCustomField8` | string |  |
| `inventoryMovements[].productCustomField9` | string |  |
| `inventoryMovements[].productHeight` | number |  |
| `inventoryMovements[].productID` | string |  |
| `inventoryMovements[].productLength` | number |  |
| `inventoryMovements[].productWeight` | number |  |
| `inventoryMovements[].productWidth` | number |  |
| `inventoryMovements[].taskID` | string |  |
| `inventoryMovements[].weightUnits` | string |  |
| `invoices[].additionalCharges[].account` | string |  |
| `invoices[].additionalCharges[].comment` | object |  |
| `invoices[].additionalCharges[].description` | string |  |
| `invoices[].additionalCharges[].discount` | number |  |
| `invoices[].additionalCharges[].price` | number |  |
| `invoices[].additionalCharges[].quantity` | number |  |
| `invoices[].additionalCharges[].tax` | number |  |
| `invoices[].additionalCharges[].taxRule` | string |  |
| `invoices[].additionalCharges[].total` | number |  |
| `invoices[].billingAddressLine1` | string |  |
| `invoices[].billingAddressLine2` | string |  |
| `invoices[].currencyConversionRate` | number |  |
| `invoices[].invoiceDate` | string |  |
| `invoices[].invoiceDueDate` | string |  |
| `invoices[].invoiceNumber` | string |  |
| `invoices[].lines[].account` | string |  |
| `invoices[].lines[].averageCost` | number |  |
| `invoices[].lines[].comment` | string |  |
| `invoices[].lines[].dimensionsUnits` | string |  |
| `invoices[].lines[].discount` | number |  |
| `invoices[].lines[].name` | string |  |
| `invoices[].lines[].price` | number |  |
| `invoices[].lines[].productCustomField1` | string |  |
| `invoices[].lines[].productCustomField10` | string |  |
| `invoices[].lines[].productCustomField2` | string |  |
| `invoices[].lines[].productCustomField3` | string |  |
| `invoices[].lines[].productCustomField4` | string |  |
| `invoices[].lines[].productCustomField5` | string |  |
| `invoices[].lines[].productCustomField6` | string |  |
| `invoices[].lines[].productCustomField7` | string |  |
| `invoices[].lines[].productCustomField8` | string |  |
| `invoices[].lines[].productCustomField9` | string |  |
| `invoices[].lines[].productHeight` | number |  |
| `invoices[].lines[].productID` | string |  |
| `invoices[].lines[].productLength` | number |  |
| `invoices[].lines[].productWeight` | number |  |
| `invoices[].lines[].productWidth` | number |  |
| `invoices[].lines[].quantity` | number |  |
| `invoices[].lines[].sku` | string |  |
| `invoices[].lines[].tax` | number |  |
| `invoices[].lines[].taxRule` | string |  |
| `invoices[].lines[].total` | number |  |
| `invoices[].lines[].weightUnits` | string |  |
| `invoices[].linkedFulfillmentNumber` | object |  |
| `invoices[].memo` | string |  |
| `invoices[].paid` | number |  |
| `invoices[].payments[].account` | string |  |
| `invoices[].payments[].amount` | number |  |
| `invoices[].payments[].currencyRate` | number |  |
| `invoices[].payments[].dateCreated` | string |  |
| `invoices[].payments[].datePaid` | string |  |
| `invoices[].payments[].id` | string |  |
| `invoices[].payments[].reference` | string |  |
| `invoices[].status` | string |  |
| `invoices[].taskID` | string |  |
| `invoices[].tax` | number |  |
| `invoices[].total` | number |  |
| `invoices[].totalBeforeTax` | number |  |
| `lastModifiedOn` | string |  |
| `location` | string |  |
| `manualJournals.status` | string |  |
| `note` | string |  |
| `order.additionalCharges[].comment` | object |  |
| `order.additionalCharges[].description` | string |  |
| `order.additionalCharges[].discount` | number |  |
| `order.additionalCharges[].price` | number |  |
| `order.additionalCharges[].quantity` | number |  |
| `order.additionalCharges[].tax` | number |  |
| `order.additionalCharges[].taxRule` | string |  |
| `order.additionalCharges[].total` | number |  |
| `order.lines[].averageCost` | number |  |
| `order.lines[].backorderQuantity` | number |  |
| `order.lines[].comment` | object |  |
| `order.lines[].dimensionsUnits` | string |  |
| `order.lines[].discount` | number |  |
| `order.lines[].dropShip` | boolean |  |
| `order.lines[].name` | string |  |
| `order.lines[].price` | number |  |
| `order.lines[].productCustomField1` | string |  |
| `order.lines[].productCustomField10` | string |  |
| `order.lines[].productCustomField2` | string |  |
| `order.lines[].productCustomField3` | string |  |
| `order.lines[].productCustomField4` | string |  |
| `order.lines[].productCustomField5` | string |  |
| `order.lines[].productCustomField6` | string |  |
| `order.lines[].productCustomField7` | string |  |
| `order.lines[].productCustomField8` | string |  |
| `order.lines[].productCustomField9` | string |  |
| `order.lines[].productHeight` | number |  |
| `order.lines[].productID` | string |  |
| `order.lines[].productLength` | number |  |
| `order.lines[].productWeight` | number |  |
| `order.lines[].productWidth` | number |  |
| `order.lines[].quantity` | number |  |
| `order.lines[].sku` | string |  |
| `order.lines[].tax` | number |  |
| `order.lines[].taxRule` | string |  |
| `order.lines[].total` | number |  |
| `order.lines[].weightUnits` | string |  |
| `order.memo` | string |  |
| `order.saleOrderNumber` | string |  |
| `order.status` | string |  |
| `order.tax` | number |  |
| `order.total` | number |  |
| `order.totalBeforeTax` | number |  |
| `phone` | string |  |
| `priceTier` | string |  |
| `quote.memo` | string |  |
| `quote.status` | string |  |
| `quote.tax` | number |  |
| `quote.total` | number |  |
| `quote.totalBeforeTax` | number |  |
| `saleOrderDate` | string |  |
| `salesRepresentative` | string |  |
| `serviceOnly` | boolean |  |
| `shipBy` | string |  |
| `shippingAddress.city` | string |  |
| `shippingAddress.company` | string |  |
| `shippingAddress.contact` | string |  |
| `shippingAddress.country` | string |  |
| `shippingAddress.displayAddressLine1` | string |  |
| `shippingAddress.displayAddressLine2` | string |  |
| `shippingAddress.id` | object |  |
| `shippingAddress.line1` | string |  |
| `shippingAddress.line2` | string |  |
| `shippingAddress.postcode` | string |  |
| `shippingAddress.shipToOther` | boolean |  |
| `shippingAddress.state` | string |  |
| `shippingNotes` | string |  |
| `skipQuote` | boolean |  |
| `sourceChannel` | string |  |
| `status` | string |  |
| `taxCalculation` | string |  |
| `taxRule` | string |  |
| `terms` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Cin7 Core API, this operation is `GET sale/attachment` (base URL `https://inventory.dearsystems.com/externalapi/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sale-attachments.md) for the provider-specific parameters and requirements.

