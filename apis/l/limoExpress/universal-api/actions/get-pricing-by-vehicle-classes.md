# LimoExpress: Get Pricing By Vehicle Classes

Retrieves pricing by vehicle class in LimoExpress.

```
GET https://connect.mindcloud.co/v1/universal/limoExpress/latest/actions/get-pricing-by-vehicle-classes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LimoExpress `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/limoExpress/latest/actions/get-pricing-by-vehicle-classes?connectionId=$CONNECTION_ID&fromLat=1&fromLng=1&pickupTime=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fromLat": "1",
  "fromLng": "1",
  "pickupTime": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/limoExpress/latest/actions/get-pricing-by-vehicle-classes?${params}`, {
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
| `fromLat` | number | yes | Pickup latitude coordinate. |
| `fromLng` | number | yes | Pickup longitude coordinate. |
| `pickupTime` | string | yes | Pickup datetime. |
| `toLat` | number | no | Dropoff latitude coordinate. |
| `toLng` | number | no | Dropoff longitude coordinate. |
| `currencyId` | string | no | Currency identifier. |
| `numberOfHours` | number | no | Total booked hours. |
| `numberOfStops` | number | no | Number of intermediate stops. |
| `numberOfChildSeats` | number | no | Number of child seats. |
| `babySeatCount` | number | no | Number of baby seats. |
| `includeTaxes` | boolean | no | Whether to include taxes in pricing. |
| `meetAndGreet` | boolean | no | Whether meet and greet is included. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "extraFees": {},
      "price": 1,
      "priceWithFees": 1,
      "vehicleClass": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `extraFees` | object | Extra fee components. |
| `price` | number | Base calculated price. |
| `priceWithFees` | number | Total price including extra fees. |
| `vehicleClass` | object | Vehicle class information. |

## Native endpoint

Through the native LimoExpress API, this operation is `POST /api/integration/pricing-by-vehicle-classes` (base URL `https://api.limoexpress.me`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pricing-by-vehicle-classes.md) for the provider-specific parameters and requirements.

