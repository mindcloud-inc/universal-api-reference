# NCEI Climate Data: List Climate Data

Finds climate data in NCEI Climate Data by dataset and date range.

```
GET https://connect.mindcloud.co/v1/universal/nCEIClimateData/latest/actions/list-climate-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NCEI Climate Data `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nCEIClimateData/latest/actions/list-climate-data?connectionId=$CONNECTION_ID&limit=25&offset=0&datasetid=GHCND&startdate=2010-05-01&enddate=2010-05-01" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "datasetid": "GHCND",
  "startdate": "2010-05-01",
  "enddate": "2010-05-01"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nCEIClimateData/latest/actions/list-climate-data?${params}`, {
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
| `datasetid` | string | yes | Required single dataset identifier, for example GHCND. Example: `GHCND`. |
| `datatypeid` | string | no | Optional data type id such as TAVG, TMIN, TMAX, or PRCP. |
| `locationid` | string | no | Optional location id such as ZIP:28801 or FIPS:37. |
| `sortfield` | string | no | Optional sort field documented by CDO. |
| `sortorder` | string | no | Sort direction: asc or desc. |
| `stationid` | string | no | Optional station id such as COOP:010008 or GHCND:USC00010008. |
| `units` | list | no | Optional units value: metric or standard. One of: `0`, `1`. |
| `startdate` | string | yes | Required start date in YYYY-MM-DD format. Use a date string, not a date-time. Example: `2010-05-01`. |
| `enddate` | string | yes | Required end date in YYYY-MM-DD format. Use a date string, not a date-time. Example: `2010-05-01`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `includemetadata` | boolean | no | Set false to skip result metadata for faster responses. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": "string",
      "datatype": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "station": "string",
      "value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | string |  |
| `datatype` | string |  |
| `date` | date |  |
| `station` | string |  |
| `value` | number |  |

## Native endpoint

Through the native NCEI Climate Data API, this operation is `GET /data` (base URL `https://www.ncei.noaa.gov/cdo-web/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-climate-data.md) for the provider-specific parameters and requirements.

