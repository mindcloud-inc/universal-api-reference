# LimoExpress: Get Extra Fees Pricing

Retrieves extra fee pricing in LimoExpress by currency and vehicle class.

```
GET https://connect.mindcloud.co/v1/universal/limoExpress/latest/actions/get-extra-fees-pricing
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LimoExpress `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/limoExpress/latest/actions/get-extra-fees-pricing?connectionId=$CONNECTION_ID&currencyId=string&vehicleClassId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "currencyId": "string",
  "vehicleClassId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/limoExpress/latest/actions/get-extra-fees-pricing?${params}`, {
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
| `currencyId` | string | yes | Currency identifier path parameter. |
| `vehicleClassId` | string | yes | Vehicle class identifier path parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "airport_fee": 1,
      "base_price": 1,
      "broken_cup_holder_fee": 1,
      "broken_glass_fee": 1,
      "child_seat_fee": 1,
      "early_late_night_fee": 1,
      "extra_stop_fee": 1,
      "fuel_surcharge_fee": 1,
      "gratuity_percentage": 1,
      "meet_and_greet_fee": 1,
      "red_carpet_fee": 1,
      "rush_hour_fee": 1,
      "smoking_fee": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `airport_fee` | number | Airport fee amount. |
| `base_price` | number | Base fee amount. |
| `broken_cup_holder_fee` | number | Broken cup holder fee amount. |
| `broken_glass_fee` | number | Broken glass fee amount. |
| `child_seat_fee` | number | Child seat fee amount. |
| `early_late_night_fee` | number | Early/late night fee amount. |
| `extra_stop_fee` | number | Extra stop fee amount. |
| `fuel_surcharge_fee` | number | Fuel surcharge fee amount. |
| `gratuity_percentage` | number | Gratuity percentage. |
| `meet_and_greet_fee` | number | Meet and greet fee amount. |
| `red_carpet_fee` | number | Red carpet fee amount. |
| `rush_hour_fee` | number | Rush hour fee amount. |
| `smoking_fee` | number | Smoking fee amount. |

## Native endpoint

Through the native LimoExpress API, this operation is `GET /api/integration/extra-fees-pricing/:currencyId/:vehicleClassId` (base URL `https://api.limoexpress.me`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-extra-fees-pricing.md) for the provider-specific parameters and requirements.

