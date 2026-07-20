# LimoExpress: Get Pricing

Retrieves pricing for coordinates in LimoExpress.

```
GET https://connect.mindcloud.co/v1/universal/limoExpress/latest/actions/get-pricing
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LimoExpress `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/limoExpress/latest/actions/get-pricing?connectionId=$CONNECTION_ID&fromLatitude=1&fromLongitude=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fromLatitude": "1",
  "fromLongitude": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/limoExpress/latest/actions/get-pricing?${params}`, {
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
| `fromLatitude` | number | yes | FROM latitude coordinate. |
| `fromLongitude` | number | yes | FROM longitude coordinate. |
| `toLatitude` | number | no | TO latitude coordinate. |
| `toLongitude` | number | no | TO longitude coordinate. |
| `currencyId` | string | no | Currency identifier. |
| `vehicleClassId` | string | no | Vehicle class identifier. |
| `distance` | number | no | Distance between start and end locations. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Pricing result rows. |
| `message` | string | Pricing calculation status message. |
| `success` | boolean | Pricing calculation success flag. |

## Native endpoint

Through the native LimoExpress API, this operation is `GET /api/integration/pricing` (base URL `https://api.limoexpress.me`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pricing.md) for the provider-specific parameters and requirements.

