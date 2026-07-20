# Carbon Intensity Universal API Examples

These examples use the MindCloud API key and Carbon Intensity connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current Carbon Intensity

Retrieves current carbon intensity for Great Britain.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/carbonIntensity/latest/actions/get-current-carbon-intensity?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/carbonIntensity/latest/actions/get-current-carbon-intensity?${params}`, {
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
        {
          "from": "string",
          "intensity": {
            "actual": 1,
            "forecast": 1,
            "index": "string"
          },
          "to": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [Get Current Carbon Intensity action reference](actions/get-current-carbon-intensity.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/carbonIntensity/latest/actions/get-current-carbon-intensity).
