# AirNow: List Monitoring Site Observations

Retrieves monitoring site observations from AirNow within a geographic area.

```
GET https://connect.mindcloud.co/v1/universal/airNow/latest/actions/list-monitoring-site-observations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AirNow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airNow/latest/actions/list-monitoring-site-observations?connectionId=$CONNECTION_ID&startDate=string&endDate=string&parameters=string&bbox=string&dataType=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "startDate": "string",
  "endDate": "string",
  "parameters": "string",
  "bbox": "string",
  "dataType": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airNow/latest/actions/list-monitoring-site-observations?${params}`, {
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
| `startDate` | string | yes | Start date/time in AirNow format, for example 2026-04-08T00. |
| `endDate` | string | yes | End date/time in AirNow format, for example 2026-04-08T01. |
| `parameters` | string | yes | Comma-separated pollutant parameters, such as OZONE,PM25. |
| `bbox` | string | yes | Bounding box in west,south,east,north order. |
| `dataType` | string | yes | A for AQI, B for concentrations, or C for both. |
| `verbose` | string | no | Set to 1 to include agency and site metadata. Default: `1`. |
| `monitorType` | string | no | Monitor type filter. Default: `0`. |
| `includeRawConcentrations` | string | no | Set to 1 to include raw concentration values when supported. Default: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agencyName": "Ava Chen",
      "aqi": 1,
      "category": 1,
      "fullAqsCode": "string",
      "intlAqsCode": "string",
      "latitude": 1,
      "longitude": 1,
      "parameter": "string",
      "siteName": "Ava Chen",
      "unit": "string",
      "utc": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agencyName` | string |  |
| `aqi` | number |  |
| `category` | number |  |
| `fullAqsCode` | string |  |
| `intlAqsCode` | string |  |
| `latitude` | number |  |
| `longitude` | number |  |
| `parameter` | string |  |
| `siteName` | string |  |
| `unit` | string |  |
| `utc` | date |  |

## Native endpoint

Through the native AirNow API, this operation is `GET /aq/data/` (base URL `https://www.airnowapi.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-monitoring-site-observations.md) for the provider-specific parameters and requirements.

