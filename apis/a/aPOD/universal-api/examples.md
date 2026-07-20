# APOD Universal API Examples

These examples use the MindCloud API key and APOD connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Today's Astronomy Picture

Retrieves today's APOD entry from NASA.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aPOD/latest/actions/get-todays-astronomy-picture?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aPOD/latest/actions/get-todays-astronomy-picture?${params}`, {
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

See the full [Get Today's Astronomy Picture action reference](actions/get-todays-astronomy-picture.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/aPOD/latest/actions/get-todays-astronomy-picture).
