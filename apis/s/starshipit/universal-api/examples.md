# Starshipit Universal API Examples

These examples use the MindCloud API key and Starshipit connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Orders (Unshipped)



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/list-orders-unshipped?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/list-orders-unshipped?${params}`, {
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
      "orders": [
        {
          "addInsurance": true,
          "addressValidation": "string",
          "archived": true,
          "carrier": "string",
          "carrierName": "Ava Chen",
          "carrierServiceCode": "string",
          "createReturn": true,
          "currency": "string",
          "dangerousGoods": true,
          "declaredValue": 1,
          "destination": {
            "building": "string",
            "city": "string",
            "company": "string",
            "country": "string",
            "deliveryInstructions": "string",
            "email": "ava@example.com",
            "name": "Ava Chen",
            "phone": "string",
            "postCode": "string",
            "state": "string",
            "street": "string",
            "taxNumbers": [
              "string"
            ]
          },
          "dtp": true,
          "insuranceValue": 1,
          "items": [
            {
              "countryOfOrigin": "string",
              "description": "string",
              "height": 1,
              "itemId": 1,
              "length": 1,
              "quantity": 1,
              "quantityToShip": 1,
              "sku": "string",
              "stockOnHand": 1,
              "value": 1,
              "weight": 1,
              "width": 1
            }
          ],
          "manifestNumber": 1,
          "metadatas": [
            {
              "metafieldKey": "string",
              "required": true,
              "value": "string"
            }
          ],
          "orderDate": "2026-05-07T12:00:00.000Z",
          "orderId": 1,
          "orderNumber": "string",
          "packages": [
            {
              "height": 1,
              "length": 1,
              "packageId": 1,
              "packagingType": "string",
              "weight": 1,
              "width": 1
            }
          ],
          "platform": "string",
          "plt": true,
          "reference": "string",
          "senderDetails": {
            "building": "string",
            "city": "string",
            "company": "string",
            "country": "string",
            "email": "ava@example.com",
            "name": "Ava Chen",
            "phone": "string",
            "postCode": "string",
            "state": "string",
            "street": "string",
            "suburb": "string",
            "taxNumbers": [
              "string"
            ]
          },
          "signatureRequired": true,
          "status": "string",
          "type": "string"
        }
      ],
      "success": true,
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

See the full [List Orders (Unshipped) action reference](actions/list-orders-unshipped.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/starshipit/latest/actions/list-orders-unshipped).

## Add Address



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/add-address" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/add-address', {
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
      "address": {
        "building": "string",
        "carrier": 1,
        "city": "string",
        "code": "string",
        "company": "string",
        "country": "string",
        "email": "ava@example.com",
        "instructions": "string",
        "name": "Ava Chen",
        "phone": "string",
        "postCode": "string",
        "signatureRequired": true,
        "state": "string",
        "street": "string",
        "suburb": "string"
      },
      "errors": [
        "string"
      ],
      "id": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Add Address action reference](actions/add-address.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/starshipit/latest/actions/add-address).
