# Zillow Econ Universal API Examples

These examples use the MindCloud API key and Zillow Econ connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get region metadata

Retrieves region metadata from Zillow Econ.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zillowEcon/latest/actions/get-region-metadata?connectionId=$CONNECTION_ID&stateCodeFIPS=48" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "stateCodeFIPS": "48"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zillowEcon/latest/actions/get-region-metadata?${params}`, {
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
      "municipalCodeFIPS": "string",
      "region": "string",
      "regionCity": "string",
      "regionCounty": "string",
      "regionID": 1,
      "regionMetro": "string",
      "regionState": "string",
      "stateCodeFIPS": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get region metadata action reference](actions/get-region-metadata.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zillowEcon/latest/actions/get-region-metadata).
