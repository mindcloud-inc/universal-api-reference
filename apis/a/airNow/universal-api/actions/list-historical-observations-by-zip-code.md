# AirNow: List Historical Observations by Zip Code

Retrieves historical air quality observations from AirNow by zip code.

```
GET https://connect.mindcloud.co/v1/universal/airNow/latest/actions/list-historical-observations-by-zip-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AirNow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airNow/latest/actions/list-historical-observations-by-zip-code?connectionId=$CONNECTION_ID&zipCode=string&date=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "zipCode": "string",
  "date": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airNow/latest/actions/list-historical-observations-by-zip-code?${params}`, {
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

Through the native AirNow API, this operation is `GET /aq/observation/zipCode/historical/` (base URL `https://www.airnowapi.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-historical-observations-by-zip-code.md) for the provider-specific parameters and requirements.

