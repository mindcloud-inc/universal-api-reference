# Hebcal Universal API Examples

These examples use the MindCloud API key and Hebcal connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Check Assur Melacha at Date Time

Checks whether work is forbidden at a date and time in Hebcal.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hebcal/latest/actions/check-assur-melacha-at-date-time?connectionId=$CONNECTION_ID&dt=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dt": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hebcal/latest/actions/check-assur-melacha-at-date-time?${params}`, {
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
      "date": "2026-05-07T12:00:00.000Z",
      "location": {
        "admin1": "string",
        "asciiname": "Ava Chen",
        "cc": "string",
        "city": "string",
        "country": "string",
        "geo": "string",
        "geonameid": 1,
        "latitude": 1,
        "longitude": 1,
        "title": "string",
        "tzid": "string"
      },
      "status": {
        "isAssurBemlacha": true,
        "localTime": "2026-05-07T12:00:00.000Z"
      },
      "version": "string"
    }
  ],
  "meta": {}
}
```

See the full [Check Assur Melacha at Date Time action reference](actions/check-assur-melacha-at-date-time.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hebcal/latest/actions/check-assur-melacha-at-date-time).
