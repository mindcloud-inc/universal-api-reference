# Amazon Seller: Get Order Address

Retrieves an order shipping address from Amazon Seller.

```
GET https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/get-order-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amazon Seller `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/get-order-address?connectionId=$CONNECTION_ID&orderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/get-order-address?${params}`, {
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
| `orderId` | string | yes | The Amazon order identifier in 3-7-7 format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amazonOrderId": "string",
      "buyerCompanyName": "Ava Chen",
      "deliveryPreferences": {
        "addressInstructions": "string",
        "otherAttributes": [
          "string"
        ],
        "preferredDeliveryTime": {
          "businessHours": [
            {
              "dayOfWeek": "string",
              "openIntervals": [
                {
                  "endTime": {
                    "hour": 1,
                    "minute": 1
                  },
                  "startTime": {
                    "hour": 1,
                    "minute": 1
                  }
                }
              ]
            }
          ]
        }
      },
      "shippingAddress": {
        "addressLine1": "string",
        "addressType": "string",
        "city": "string",
        "countryCode": "string",
        "name": "Ava Chen",
        "postalCode": "string",
        "stateOrRegion": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amazonOrderId` | string |  |
| `buyerCompanyName` | string |  |
| `deliveryPreferences.addressInstructions` | string |  |
| `deliveryPreferences.otherAttributes[]` | string |  |
| `deliveryPreferences.preferredDeliveryTime.businessHours[].dayOfWeek` | string |  |
| `deliveryPreferences.preferredDeliveryTime.businessHours[].openIntervals[].endTime.hour` | number |  |
| `deliveryPreferences.preferredDeliveryTime.businessHours[].openIntervals[].endTime.minute` | number |  |
| `deliveryPreferences.preferredDeliveryTime.businessHours[].openIntervals[].startTime.hour` | number |  |
| `deliveryPreferences.preferredDeliveryTime.businessHours[].openIntervals[].startTime.minute` | number |  |
| `shippingAddress.addressLine1` | string |  |
| `shippingAddress.addressType` | string |  |
| `shippingAddress.city` | string |  |
| `shippingAddress.countryCode` | string |  |
| `shippingAddress.name` | string |  |
| `shippingAddress.postalCode` | string |  |
| `shippingAddress.stateOrRegion` | string |  |

## Native endpoint

Through the native Amazon Seller API, this operation is `GET orders/v0/orders/:orderId/address` (base URL `https://{{credentials.environment}}-{{credentials.region}}.amazon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order-address.md) for the provider-specific parameters and requirements.

