# Storm Glass Universal API Examples

These examples use the MindCloud API key and Storm Glass connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Astronomy

Retrieves astronomy data from Storm Glass.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stormGlass/latest/actions/get-astronomy?connectionId=$CONNECTION_ID&lat=37.7749&lng=-122.4194" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "lat": "37.7749",
  "lng": "-122.4194"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stormGlass/latest/actions/get-astronomy?${params}`, {
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
      "data": [
        {}
      ],
      "meta": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Astronomy action reference](actions/get-astronomy.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/stormGlass/latest/actions/get-astronomy).
