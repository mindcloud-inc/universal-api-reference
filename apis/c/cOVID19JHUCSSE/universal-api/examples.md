# COVID-19 JHU CSSE Universal API Examples

These examples use the MindCloud API key and COVID-19 JHU CSSE connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Latest Global Daily Report

Retrieves the latest archived global COVID-19 daily report rows.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cOVID19JHUCSSE/latest/actions/list-latest-global-daily-report?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cOVID19JHUCSSE/latest/actions/list-latest-global-daily-report?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "active": 1,
      "admin2": "string",
      "caseFatalityRatio": 1,
      "combinedKey": "string",
      "confirmed": 1,
      "countryRegion": "string",
      "deaths": 1,
      "fips": 1,
      "incidentRate": 1,
      "lastUpdate": "2026-05-07T12:00:00.000Z",
      "lat": 1,
      "long": 1,
      "provinceState": "string",
      "recovered": 1
    }
  ],
  "meta": {}
}
```

See the full [List Latest Global Daily Report action reference](actions/list-latest-global-daily-report.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cOVID19JHUCSSE/latest/actions/list-latest-global-daily-report).
