# Cin7 Core Universal API Examples

These examples use the MindCloud API key and Cin7 Core connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Sale



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cin7core/latest/actions/get-sale?connectionId=$CONNECTION_ID&ID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cin7core/latest/actions/get-sale?${params}`, {
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

See the full [Get Sale action reference](actions/get-sale.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cin7core/latest/actions/get-sale).

## Create Carrier



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cin7core/latest/actions/create-carrier" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "Description": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cin7core/latest/actions/create-carrier', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "Description": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Create Carrier action reference](actions/create-carrier.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cin7core/latest/actions/create-carrier).
