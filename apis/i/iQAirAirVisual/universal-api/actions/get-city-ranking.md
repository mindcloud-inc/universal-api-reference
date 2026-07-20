# IQAir AirVisual: Get City Ranking



```
GET https://connect.mindcloud.co/v1/universal/iQAirAirVisual/latest/actions/get-city-ranking
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IQAir AirVisual `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iQAirAirVisual/latest/actions/get-city-ranking?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iQAirAirVisual/latest/actions/get-city-ranking?${params}`, {
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
| `sort` | string | no | Optional ranking order: asc for cleanest cities or desc for most polluted cities. Example: `desc`. |
| `country` | string | no | Optional country filter. Allowed documented values include Thailand, USA, and Canada. Example: `USA`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "city": "string",
      "country": "string",
      "ranking": {
        "currentAqi": 1,
        "currentAqiCn": 1,
        "lastAqi": 1,
        "lastAqiCn": 1
      },
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city` | string | Ranked city name. |
| `country` | string | Country for the ranked city. |
| `ranking` | object | Ranking metrics for the city. |
| `ranking.currentAqi` | number | Current AQI ranking value. |
| `ranking.currentAqiCn` | number | Current China AQI ranking value. |
| `ranking.lastAqi` | number | Previous AQI ranking value when present. |
| `ranking.lastAqiCn` | number | Previous China AQI ranking value when present. |
| `state` | string | State for the ranked city. |

## Native endpoint

Through the native IQAir AirVisual API, this operation is `GET /v2/city_ranking` (base URL `https://api.airvisual.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-city-ranking.md) for the provider-specific parameters and requirements.

