# Amazon Seller Universal API Examples

These examples use the MindCloud API key and Amazon Seller connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Marketplace Participations

Retrieves marketplace participations from Amazon Seller.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/get-marketplace-participations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/get-marketplace-participations?${params}`, {
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
      "amazonOrderId": "string",
      "automatedShippingSettings": {
        "automatedCarrier": "string",
        "automatedCarrierName": "Ava Chen",
        "automatedShipMethod": "string",
        "automatedShipMethodName": "Ava Chen",
        "hasAutomatedShippingSettings": true
      },
      "buyerInfo": {
        "buyerEmail": "ava@example.com"
      },
      "defaultShipFromLocationAddress": {
        "addressLine1": "string",
        "city": "string",
        "countryCode": "string",
        "name": "Ava Chen",
        "postalCode": "string",
        "stateOrRegion": "string"
      },
      "earliestDeliveryDate": "string",
      "earliestShipDate": "string",
      "fulfillmentChannel": "string",
      "hasRegulatedItems": true,
      "isAccessPointOrder": true,
      "isBusinessOrder": true,
      "isGlobalExpressEnabled": true,
      "isISPU": true,
      "isPremiumOrder": true,
      "isPrime": true,
      "isReplacementOrder": "string",
      "isSoldByAB": true,
      "lastUpdateDate": "string",
      "latestDeliveryDate": "string",
      "latestShipDate": "string",
      "marketplaceId": "string",
      "numberOfItemsShipped": 1,
      "numberOfItemsUnshipped": 1,
      "orderStatus": "string",
      "orderTotal": {
        "amount": "string",
        "currencyCode": "string"
      },
      "orderType": "string",
      "paymentMethod": "string",
      "paymentMethodDetails": [
        "string"
      ],
      "purchaseDate": "string",
      "salesChannel": "string",
      "shipmentServiceLevelCategory": "string",
      "shippingAddress": {
        "city": "string",
        "countryCode": "string",
        "postalCode": "string",
        "stateOrRegion": "string"
      },
      "shipServiceLevel": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Marketplace Participations action reference](actions/get-marketplace-participations.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/amazonSeller/latest/actions/get-marketplace-participations).

## Confirm Shipment

Updates shipment confirmation for an Amazon Seller order.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/confirm-shipment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orderId": "string",
  "marketplaceId": "string",
  "packageReferenceId": "string",
  "shipDate": "string",
  "carrierCode": "string",
  "trackingNumber": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/confirm-shipment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orderId": "string",
    "marketplaceId": "string",
    "packageReferenceId": "string",
    "shipDate": "string",
    "carrierCode": "string",
    "trackingNumber": "string"
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
      "orderId": "string",
      "packageReferenceId": "string",
      "shipDate": "string",
      "trackingNumber": "string"
    }
  ],
  "meta": {}
}
```

See the full [Confirm Shipment action reference](actions/confirm-shipment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/amazonSeller/latest/actions/confirm-shipment).
