# NCEI Climate Data: List Stations

Finds weather stations in NCEI Climate Data by filter criteria.

```
GET https://connect.mindcloud.co/v1/universal/nCEIClimateData/latest/actions/list-stations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NCEI Climate Data `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nCEIClimateData/latest/actions/list-stations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nCEIClimateData/latest/actions/list-stations?${params}`, {
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
| `datasetid` | string | no | Filter stations by dataset id, such as GHCND. |
| `datatypeid` | string | no | Filter stations by data type id, such as TAVG. |
| `extent` | string | no | Geographic bounding box as south,west,north,east coordinates. |
| `locationid` | string | no | Filter stations by location id, such as FIPS:37. |

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

Through the native NCEI Climate Data API, this operation is `GET /stations` (base URL `https://www.ncei.noaa.gov/cdo-web/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-stations.md) for the provider-specific parameters and requirements.

