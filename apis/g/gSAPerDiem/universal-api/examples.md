# GSA Per Diem Universal API Examples

These examples use the MindCloud API key and GSA Per Diem connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List CONUS M&IE Breakdown Rates

Retrieves CONUS M&IE breakdown rates from GSA Per Diem.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gSAPerDiem/latest/actions/list-conus-mie-breakdown-rates?connectionId=$CONNECTION_ID&year=2026" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "year": "2026"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gSAPerDiem/latest/actions/list-conus-mie-breakdown-rates?${params}`, {
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
      "breakfast": 1,
      "dinner": 1,
      "FirstLastDay": 1,
      "incidental": 1,
      "lunch": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

See the full [List CONUS M&IE Breakdown Rates action reference](actions/list-conus-mie-breakdown-rates.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/gSAPerDiem/latest/actions/list-conus-mie-breakdown-rates).
