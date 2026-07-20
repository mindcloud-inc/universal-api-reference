# US Congress CRS Universal API Examples

These examples use the MindCloud API key and US Congress CRS connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List CRS Reports

Retrieves CRS reports from US Congress CRS.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uSCongressCRS/latest/actions/list-crs-reports?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uSCongressCRS/latest/actions/list-crs-reports?${params}`, {
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
      "CRSReports": [
        {}
      ],
      "pagination": {},
      "request": {}
    }
  ],
  "meta": {}
}
```

See the full [List CRS Reports action reference](actions/list-crs-reports.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/uSCongressCRS/latest/actions/list-crs-reports).
