# Easyship: Request Rates

Retrieves shipping rates from Easyship.

```
GET https://connect.mindcloud.co/v1/universal/easyship/latest/actions/request-rates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Easyship `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyship/latest/actions/request-rates?connectionId=$CONNECTION_ID&originAddress=%5Bobject%20Object%5D&destinationAddress=%5Bobject%20Object%5D&parcels%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "originAddress": "[object Object]",
  "destinationAddress": "[object Object]",
  "parcels[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyship/latest/actions/request-rates?${params}`, {
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
| `originAddress` | object | yes | Origin address object for the shipment rate request. |
| `destinationAddress` | object | yes | Destination address object for the shipment rate request. |
| `parcels[]` | array<object> | yes | Parcels array for the shipment rate request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "availableHandoverOptions": [
        "string"
      ],
      "costRank": 1,
      "courierService": {
        "id": "string",
        "name": "Ava Chen",
        "umbrellaName": "Ava Chen"
      },
      "currency": "string",
      "deliveryTimeRank": 1,
      "description": "string",
      "fullDescription": "string",
      "incoterms": "string",
      "maxDeliveryTime": 1,
      "minDeliveryTime": 1,
      "paymentRecipient": "string",
      "shipmentChargeTotal": 1,
      "totalCharge": 1,
      "valueForMoneyRank": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availableHandoverOptions` | array<string> |  |
| `costRank` | number |  |
| `courierService.id` | string |  |
| `courierService.name` | string |  |
| `courierService.umbrellaName` | string |  |
| `currency` | string |  |
| `deliveryTimeRank` | number |  |
| `description` | string |  |
| `fullDescription` | string |  |
| `incoterms` | string |  |
| `maxDeliveryTime` | number |  |
| `minDeliveryTime` | number |  |
| `paymentRecipient` | string |  |
| `shipmentChargeTotal` | number |  |
| `totalCharge` | number |  |
| `valueForMoneyRank` | number |  |

## Native endpoint

Through the native Easyship API, this operation is `POST /rates` (base URL `https://public-api.easyship.com/2024-09`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/request-rates.md) for the provider-specific parameters and requirements.

