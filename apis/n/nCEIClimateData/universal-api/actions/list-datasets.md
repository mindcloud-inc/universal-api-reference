# NCEI Climate Data: List Datasets

Finds climate datasets in NCEI Climate Data by filter criteria.

```
GET https://connect.mindcloud.co/v1/universal/nCEIClimateData/latest/actions/list-datasets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NCEI Climate Data `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nCEIClimateData/latest/actions/list-datasets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nCEIClimateData/latest/actions/list-datasets?${params}`, {
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
| `datatypeid` | string | no | Filter datasets by data type id, such as TAVG or TOBS. |
| `enddate` | string | no | Filter datasets that have data before this YYYY-MM-DD date. Example: `2012-09-10`. |
| `locationid` | string | no | Filter datasets by location id, such as FIPS:37 or ZIP:28801. |
| `sortfield` | string | no | Sort by id, name, mindate, maxdate, or datacoverage. |
| `sortorder` | string | no | Sort direction: asc or desc. |
| `startdate` | string | no | Filter datasets that have data after this YYYY-MM-DD date. Example: `1970-10-03`. |
| `stationid` | string | no | Filter datasets by station id, such as COOP:010957. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "datacoverage": 1,
      "id": "string",
      "maxdate": "2026-05-07T12:00:00.000Z",
      "mindate": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "uid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `datacoverage` | number |  |
| `id` | string |  |
| `maxdate` | date |  |
| `mindate` | date |  |
| `name` | string |  |
| `uid` | string |  |

## Native endpoint

Through the native NCEI Climate Data API, this operation is `GET /datasets` (base URL `https://www.ncei.noaa.gov/cdo-web/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-datasets.md) for the provider-specific parameters and requirements.

