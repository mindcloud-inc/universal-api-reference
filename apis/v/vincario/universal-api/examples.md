# Vincario Universal API Examples

These examples use the MindCloud API key and Vincario connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Balance



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vincario/latest/actions/get-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vincario/latest/actions/get-balance?${params}`, {
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
      "apiOcrVinScanner": 1,
      "apiOemVinLookup": 1,
      "apiStolenCheck": 1,
      "apiVehicleMarketValue": 1,
      "apiVinDecode": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Balance action reference](actions/get-balance.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/vincario/latest/actions/get-balance).
