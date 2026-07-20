# NCEI Climate Data: Get Station

Retrieves station details from NCEI Climate Data.

```
GET https://connect.mindcloud.co/v1/universal/nCEIClimateData/latest/actions/get-station
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NCEI Climate Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nCEIClimateData/latest/actions/get-station?connectionId=$CONNECTION_ID&stationId=COOP%3A010008" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "stationId": "COOP:010008"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nCEIClimateData/latest/actions/get-station?${params}`, {
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
| `stationId` | string | yes | Station identifier to retrieve, for example COOP:010008. Example: `COOP:010008`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "datacoverage": 1,
      "elevation": 1,
      "elevationUnit": "string",
      "id": "string",
      "latitude": 1,
      "longitude": 1,
      "maxdate": "2026-05-07T12:00:00.000Z",
      "mindate": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `datacoverage` | number |  |
| `elevation` | number |  |
| `elevationUnit` | string |  |
| `id` | string |  |
| `latitude` | number |  |
| `longitude` | number |  |
| `maxdate` | date |  |
| `mindate` | date |  |
| `name` | string |  |

## Native endpoint

Through the native NCEI Climate Data API, this operation is `GET /stations/[:stationId]` (base URL `https://www.ncei.noaa.gov/cdo-web/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-station.md) for the provider-specific parameters and requirements.

