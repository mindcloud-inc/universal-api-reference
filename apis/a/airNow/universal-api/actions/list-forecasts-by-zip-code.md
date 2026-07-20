# AirNow: List Forecasts by Zip Code

Retrieves air quality forecasts from AirNow by zip code.

```
GET https://connect.mindcloud.co/v1/universal/airNow/latest/actions/list-forecasts-by-zip-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AirNow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airNow/latest/actions/list-forecasts-by-zip-code?connectionId=$CONNECTION_ID&zipCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "zipCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airNow/latest/actions/list-forecasts-by-zip-code?${params}`, {
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
| `zipCode` | string | yes | The zip code used to resolve the reporting area. |
| `date` | string | no | Forecast start date in YYYY-MM-DD format. |
| `distance` | number | no | Search radius in miles. Default: `25`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actionDay": true,
      "aqi": 1,
      "category": {
        "name": "Ava Chen",
        "number": 1
      },
      "dateForecast": "2026-05-07T12:00:00.000Z",
      "dateIssue": "2026-05-07T12:00:00.000Z",
      "discussion": "string",
      "latitude": 1,
      "longitude": 1,
      "parameterName": "Ava Chen",
      "reportingArea": "string",
      "stateCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actionDay` | boolean |  |
| `aqi` | number |  |
| `category.name` | string |  |
| `category.number` | number |  |
| `dateForecast` | date |  |
| `dateIssue` | date |  |
| `discussion` | string |  |
| `latitude` | number |  |
| `longitude` | number |  |
| `parameterName` | string |  |
| `reportingArea` | string |  |
| `stateCode` | string |  |

## Native endpoint

Through the native AirNow API, this operation is `GET /aq/forecast/zipCode/` (base URL `https://www.airnowapi.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-forecasts-by-zip-code.md) for the provider-specific parameters and requirements.

