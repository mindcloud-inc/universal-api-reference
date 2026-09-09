# Walmart Universal API Examples

These examples use the MindCloud API key and Walmart connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Token Detail

Returns OAuth token metadata and scopes granted by the seller to your application. Use this to verify whether a token is valid, when it expires, and which API categories are allowed (full_access, view_only, no_access).

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-token-detail?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-token-detail?${params}`, {
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
      "expireAt": "string",
      "isChannelMatch": true,
      "issuedAt": "string",
      "isValid": true,
      "scopes": {
        "content": "string",
        "feeds": "string",
        "fulfillment": "string",
        "inventory": "string",
        "item": "string",
        "lagtime": "string",
        "orders": "string",
        "price": "string",
        "profile": "string",
        "promo": "string",
        "report": "string",
        "reports": "string",
        "repricer": "string",
        "returns": "string",
        "rules": "string",
        "shipping": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Token Detail action reference](actions/get-token-detail.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/walmart/latest/actions/get-token-detail).

## Acknowledge Orders

Acknowledge an entire order, including all of its order lines.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/acknowledge-orders" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "purchaseOrderId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/walmart/latest/actions/acknowledge-orders', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "purchaseOrderId": "string"
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
      "customerEmailId": "ava@example.com",
      "customerOrderId": "string",
      "orderDate": 1,
      "orderLines": {
        "orderLine": [
          {
            "charges": {
              "charge": [
                {
                  "chargeAmount": {
                    "amount": 1,
                    "currency": "string"
                  },
                  "chargeName": "Ava Chen",
                  "chargeType": "string",
                  "tax": {
                    "taxAmount": {
                      "amount": 1,
                      "currency": "string"
                    },
                    "taxName": "Ava Chen"
                  }
                }
              ]
            },
            "fulfillment": {
              "fulfillmentOption": "string",
              "pickUpDateTime": 1,
              "shipMethod": "string",
              "shippingConfigSource": "string",
              "shippingProgramType": "string",
              "shippingSLA": "string"
            },
            "item": {
              "productName": "Ava Chen",
              "sku": "string"
            },
            "lineNumber": "string",
            "orderLineQuantity": {
              "amount": "string",
              "unitOfMeasurement": "string"
            },
            "orderLineStatuses": {
              "orderLineStatus": [
                {
                  "cancellationReason": "string",
                  "status": "string",
                  "statusQuantity": {
                    "amount": "string",
                    "unitOfMeasurement": "string"
                  }
                }
              ]
            },
            "statusDate": 1
          }
        ]
      },
      "purchaseOrderId": "string",
      "shipNode": {
        "type": "string"
      },
      "shippingInfo": {
        "estimatedDeliveryDate": 1,
        "estimatedShipDate": 1,
        "methodCode": "string",
        "phone": "string",
        "postalAddress": {
          "address1": "string",
          "addressType": "string",
          "city": "string",
          "country": "string",
          "name": "Ava Chen",
          "postalCode": "string",
          "state": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

See the full [Acknowledge Orders action reference](actions/acknowledge-orders.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/walmart/latest/actions/acknowledge-orders).
