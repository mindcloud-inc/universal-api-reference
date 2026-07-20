# National Weather Service: Get Gridpoint Forecast

Retrieves the forecast for a National Weather Service gridpoint.

```
GET https://connect.mindcloud.co/v1/universal/nationalWeatherService/latest/actions/get-gridpoint-forecast
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a National Weather Service `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nationalWeatherService/latest/actions/get-gridpoint-forecast?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nationalWeatherService/latest/actions/get-gridpoint-forecast?${params}`, {
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
| `wfo` | string | no | Weather Forecast Office identifier. |
| `x` | string | no | Gridpoint X coordinate. |
| `y` | string | no | Gridpoint Y coordinate. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native National Weather Service API returns.

## Native endpoint

Through the native National Weather Service API, this operation is `GET /gridpoints/:wfo/:x,:y/forecast` (base URL `https://api.weather.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-gridpoint-forecast.md) for the provider-specific parameters and requirements.

