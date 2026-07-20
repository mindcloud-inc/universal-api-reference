# IQAir AirVisual Universal API Examples

These examples use the MindCloud API key and IQAir AirVisual connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Countries



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iQAirAirVisual/latest/actions/list-countries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iQAirAirVisual/latest/actions/list-countries?${params}`, {
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
      "country": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Countries action reference](actions/list-countries.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/iQAirAirVisual/latest/actions/list-countries).
