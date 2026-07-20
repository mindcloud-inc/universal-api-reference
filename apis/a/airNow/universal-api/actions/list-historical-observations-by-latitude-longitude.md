# AirNow: List Historical Observations by Latitude Longitude

Retrieves historical air quality observations from AirNow by latitude and longitude.

```
GET https://connect.mindcloud.co/v1/universal/airNow/latest/actions/list-historical-observations-by-latitude-longitude
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AirNow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airNow/latest/actions/list-historical-observations-by-latitude-longitude?connectionId=$CONNECTION_ID&latitude=1&longitude=1&date=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "latitude": "1",
  "longitude": "1",
  "date": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airNow/latest/actions/list-historical-observations-by-latitude-longitude?${params}`, {
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
| `latitude` | number | yes | Latitude for the requested location. |
| `longitude` | number | yes | Longitude for the requested location. |
| `date` | string | yes | Historical observation timestamp in AirNow format, for example 2026-04-08T00-0000. |
| `distance` | number | no | Search radius in miles. Default: `25`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aqi": 1,
      "category": {
        "name": "Ava Chen",
        "number": 1
      },
      "dateObserved": "2026-05-07T12:00:00.000Z",
      "hourObserved": 1,
      "latitude": 1,
      "localTimeZone": "string",
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
| `aqi` | number |  |
| `category.name` | string |  |
| `category.number` | number |  |
| `dateObserved` | date |  |
| `hourObserved` | number |  |
| `latitude` | number |  |
| `localTimeZone` | string |  |
| `longitude` | number |  |
| `parameterName` | string |  |
| `reportingArea` | string |  |
| `stateCode` | string |  |

## Native endpoint

Through the native AirNow API, this operation is `GET /aq/observation/latLong/historical/` (base URL `https://www.airnowapi.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-historical-observations-by-latitude-longitude.md) for the provider-specific parameters and requirements.

