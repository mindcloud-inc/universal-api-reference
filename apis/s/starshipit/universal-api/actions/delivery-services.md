# Starshipit: Delivery Services



```
GET https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/delivery-services
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Starshipit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/delivery-services?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/delivery-services?${params}`, {
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
| `orderId` | number | no |  |
| `refreshRate` | boolean | no |  |
| `sender.street` | string | no |  |
| `sender.suburb` | string | no |  |
| `sender.city` | string | no |  |
| `sender.state` | string | no |  |
| `sender.postCode` | string | no |  |
| `sender.countryCode` | string | no |  |
| `destination.street` | string | no |  |
| `destination.suburb` | string | no |  |
| `destination.city` | string | no |  |
| `destination.state` | string | no |  |
| `destination.postCode` | string | no |  |
| `destination.countryCode` | string | no |  |
| `packages[]` | array<object> | no |  |
| `declaredValue` | number | no |  |
| `returnOrder` | boolean | no |  |
| `includePricing` | boolean | no |  |
| `signatureRequired` | string | no |  |
| `authorityToLeave` | boolean | no |  |
| `dangerousGoods` | boolean | no |  |
| `insuranceValue` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": [
        "string"
      ],
      "services": [
        {
          "carrier": "string",
          "carrierName": "Ava Chen",
          "metafields": [
            {
              "defaultValue": "string",
              "description": "string",
              "displayType": "string",
              "key": "string",
              "label": "string",
              "name": "Ava Chen",
              "readOnly": true,
              "value": "string",
              "valueType": "string"
            }
          ],
          "pricingBreakdown": {
            "calculatedGST": "string",
            "calculatedPrice": "string",
            "calculatedPriceExGST": "string",
            "estimatedDeliveryDate": "2026-05-07T12:00:00.000Z",
            "estimatedDeliveryDaysEarliest": "string",
            "estimatedDeliveryDaysLatest": "string"
          },
          "serviceCode": "string",
          "serviceName": "Ava Chen",
          "totalPrice": 1
        }
      ],
      "submitActualShippingCost": true,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors` | array<string> |  |
| `services` | array<object> |  |
| `services[].carrier` | string |  |
| `services[].carrierName` | string |  |
| `services[].metafields` | array<object> |  |
| `services[].metafields[].defaultValue` | string |  |
| `services[].metafields[].description` | string |  |
| `services[].metafields[].displayType` | string |  |
| `services[].metafields[].key` | string |  |
| `services[].metafields[].label` | string |  |
| `services[].metafields[].name` | string |  |
| `services[].metafields[].readOnly` | boolean |  |
| `services[].metafields[].value` | string |  |
| `services[].metafields[].valueType` | string |  |
| `services[].pricingBreakdown` | object |  |
| `services[].pricingBreakdown.calculatedGST` | string |  |
| `services[].pricingBreakdown.calculatedPrice` | string |  |
| `services[].pricingBreakdown.calculatedPriceExGST` | string |  |
| `services[].pricingBreakdown.estimatedDeliveryDate` | date |  |
| `services[].pricingBreakdown.estimatedDeliveryDaysEarliest` | string |  |
| `services[].pricingBreakdown.estimatedDeliveryDaysLatest` | string |  |
| `services[].serviceCode` | string |  |
| `services[].serviceName` | string |  |
| `services[].totalPrice` | number |  |
| `submitActualShippingCost` | boolean |  |
| `success` | boolean |  |

## Native endpoint

Through the native Starshipit API, this operation is `POST /deliveryservices` (base URL `https://api.starshipit.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delivery-services.md) for the provider-specific parameters and requirements.

