# Beds24: List Fixed Prices

Retrieves fixed prices from Beds24.

```
GET https://connect.mindcloud.co/v1/universal/beds24/latest/actions/list-fixed-prices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Beds24 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/beds24/latest/actions/list-fixed-prices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/beds24/latest/actions/list-fixed-prices?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "firstNight": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "lastNight": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "offerId": 1,
      "propertyId": 1,
      "roomId": 1,
      "roomPrice": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `firstNight` | date |  |
| `id` | number |  |
| `lastNight` | date |  |
| `name` | string |  |
| `offerId` | number |  |
| `propertyId` | number |  |
| `roomId` | number |  |
| `roomPrice` | number |  |

## Native endpoint

Through the native Beds24 API, this operation is `GET /inventory/fixedPrices` (base URL `https://beds24.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-fixed-prices.md) for the provider-specific parameters and requirements.

