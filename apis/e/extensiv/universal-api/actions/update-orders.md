# Extensiv Order Manager: Update Orders

Updates orders in Extensiv Order Manager.

```
POST https://connect.mindcloud.co/v1/universal/extensiv/latest/actions/update-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Extensiv Order Manager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/extensiv/latest/actions/update-orders" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/extensiv/latest/actions/update-orders', {
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
| `amountPaid` | object | no |  |
| `amountPaid.amount` | number | no |  |
| `customShipBilling.accountNumber` | string | no |  |
| `customShipBilling.codAmount.amount` | number | no |  |
| `fulfillmentSource.name` | string | no |  |
| `orderIdentifier.orderId` | number | no |  |
| `shipMethod.ltlFtlShipment` | object | no | Less Than Truckload Full Truckload Shipment |
| `shipMethod.ltlFtlShipment.boxCount` | number | no |  |
| `amountPaid.currency` | string | no |  |
| `customField1` | string | no |  |
| `customShipBilling.billingZipCode` | string | no |  |
| `customShipBilling.codAmount.currency` | string | no |  |
| `fulfillmentSource.warehouseId` | number | no |  |
| `orderIdentifier.orderNumber` | string | no |  |
| `shipMethod.ltlFtlShipment.freightReadyDate` | string | no |  |
| `shipMethod.shippingCarrier` | string | no |  |
| `customField2` | string | no |  |
| `customShipBilling.codAmount` | object | no |  |
| `orderIdentifier.salesChannelId` | number | no |  |
| `shipMethod.ltlFtlShipment.id` | number | no |  |
| `shipMethod.shippingProviderId` | number | no |  |
| `customField3` | string | no |  |
| `customShipBilling.country` | string | no |  |
| `shipMethod.ltlFtlShipment.liabilityCoverage` | number | no |  |
| `shipMethod.shippingServiceId` | number | no |  |
| `customShipBilling` | object | no |  |
| `shipMethod.ltlFtlShipment.liabilityType` | string | no |  |
| `shipMethod.packageTypeId` | number | no |  |
| `customShipBillingOption` | list<string> | no |  |
| `shipMethod.ltlFtlShipment.measurementUnitId` | number | no |  |
| `fulfillmentSource` | object | no |  |
| `gift` | boolean | no |  |
| `giftMessage` | string | no |  |
| `height` | number | no |  |
| `internalNotes` | string | no |  |
| `length` | number | no |  |
| `orderIdentifier` | object | no |  |
| `paymentDate` | string | no |  |
| `receiveByDate` | string | no |  |
| `shipAddress1` | string | no |  |
| `shipAddress2` | string | no |  |
| `shipAddress3` | string | no |  |
| `shipByDate` | string | no |  |
| `shipCity` | string | no |  |
| `shipCompany` | string | no |  |
| `shipCountry` | string | no |  |
| `shipMethod` | object | no |  |
| `shipName` | string | no |  |
| `shipPhone` | string | no |  |
| `shipState` | string | no |  |
| `shipZipCode` | string | no |  |
| `weight` | number | no |  |
| `width` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": [
        {}
      ],
      "message": "string",
      "results": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors` | array<object> | Validation errors returned by the API. |
| `message` | string | Bulk update result message. |
| `results` | array<object> | Bulk update result records. |

## Native endpoint

Through the native Extensiv Order Manager API, this operation is `POST /v1.1/orders` (base URL `https://api.skubana.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-orders.md) for the provider-specific parameters and requirements.

