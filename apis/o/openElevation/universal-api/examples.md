# Open-Elevation Universal API Examples

These examples use the MindCloud API key and Open-Elevation connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Look Up Elevation

Retrieves elevations from Open-Elevation for coordinates in the query string.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openElevation/latest/actions/look-up-elevation?connectionId=$CONNECTION_ID&locations=41.161758%2C-8.583933" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "locations": "41.161758,-8.583933"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openElevation/latest/actions/look-up-elevation?${params}`, {
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
      "elevation": 1,
      "latitude": 1,
      "longitude": 1
    }
  ],
  "meta": {}
}
```

See the full [Look Up Elevation action reference](actions/look-up-elevation.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/openElevation/latest/actions/look-up-elevation).
