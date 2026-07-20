# AccuWeather: Get Tropical Storm Forecasts

Retrieves tropical storm forecasts from AccuWeather by year, basin, and government ID.

```
GET https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/get-tropical-storm-forecasts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AccuWeather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/get-tropical-storm-forecasts?connectionId=$CONNECTION_ID&basin=AL&govId=2&year=2024" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "basin": "AL",
  "govId": "2",
  "year": "2024"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/get-tropical-storm-forecasts?${params}`, {
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
| `basin` | string | yes | Required tropical basin code. Default: `AL`. |
| `govId` | string | yes | Required government storm ID. Default: `2`. |
| `year` | string | yes | Required four-digit year. Default: `2024`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Category": "string",
      "DateTime": "string",
      "Latitude": 1,
      "Longitude": 1,
      "Text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Category` | string |  |
| `DateTime` | string |  |
| `Latitude` | number |  |
| `Longitude` | number |  |
| `Text` | string |  |

## Native endpoint

Through the native AccuWeather API, this operation is `GET /tropical/v1/gov/storms/:year/:basin/:govId/forecasts` (base URL `https://dataservice.accuweather.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tropical-storm-forecasts.md) for the provider-specific parameters and requirements.

