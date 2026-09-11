# BigCommerce (B2B) Universal API Examples

These examples use the MindCloud API key and BigCommerce (B2B) connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get invoices



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bigCommerceB2B/latest/actions/get-invoices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bigCommerceB2B/latest/actions/get-invoices?${params}`, {
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
      "bcGroupName": "Ava Chen",
      "bcId": 1,
      "channelId": "string",
      "channelName": "Ava Chen",
      "createdAt": 1,
      "customerBcGroupName": {},
      "customerBcId": {},
      "customerId": "string",
      "customerName": "Ava Chen",
      "details": {
        "details": {
          "lineItems": [
            {
              "comments": "string",
              "description": "string",
              "productId": 1,
              "quantity": 1,
              "sku": "string",
              "type": "string",
              "unitDiscount": {
                "code": "string",
                "value": 1
              },
              "unitPrice": {
                "code": "string",
                "value": "string"
              }
            }
          ]
        },
        "header": {
          "billingAddress": {
            "city": "string",
            "country": "string",
            "firstName": "Ava",
            "lastName": "Chen",
            "state": "string",
            "street1": "string",
            "street2": "string",
            "zipCode": "string"
          },
          "costLines": [
            {
              "amount": {
                "code": "string",
                "value": "string"
              },
              "description": "string"
            }
          ],
          "orderDate": 1
        },
        "type": "string"
      },
      "dueDate": 1,
      "externalCustomerId": {},
      "externalId": {},
      "externalPdfUrl": {},
      "id": 1,
      "invoiceNumber": "string",
      "notAllowedPay": 1,
      "openBalance": {
        "code": "string",
        "value": "string"
      },
      "orderNumber": 1,
      "originalBalance": {
        "code": "string",
        "value": "string"
      },
      "pendingPaymentCount": 1,
      "purchaseOrderNumber": {},
      "source": 1,
      "status": 1,
      "storeHash": "string",
      "termsConditions": "string",
      "type": "string",
      "updatedAt": 1
    }
  ],
  "meta": {}
}
```

See the full [Get invoices action reference](actions/get-invoices.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bigCommerceB2B/latest/actions/get-invoices).

## Create Invoice



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bigCommerceB2B/latest/actions/create-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "invoiceNumber": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bigCommerceB2B/latest/actions/create-invoice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "invoiceNumber": "string"
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

See the full [Create Invoice action reference](actions/create-invoice.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bigCommerceB2B/latest/actions/create-invoice).
