# NASA APOD Universal API Examples

These examples use the MindCloud API key and NASA APOD connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get APOD Date Range



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nASAAPOD/latest/actions/get-apod-date-range?connectionId=$CONNECTION_ID&start_date=2026-05-07T12%3A00%3A00.000Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "start_date": "2026-05-07T12:00:00.000Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nASAAPOD/latest/actions/get-apod-date-range?${params}`, {
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
      "copyright": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "explanation": "string",
      "hdurl": "https://example.com",
      "media_type": "string",
      "service_version": "string",
      "thumbnail_url": "https://example.com",
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Get APOD Date Range action reference](actions/get-apod-date-range.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/nASAAPOD/latest/actions/get-apod-date-range).
