# Chicago Transit Authority Universal API Examples

These examples use the MindCloud API key and Chicago Transit Authority connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Train Arrivals by Station

Retrieves train arrival predictions in Chicago Transit Authority by station.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chicagoTransitAuthority/latest/actions/get-train-arrivals-by-station?connectionId=$CONNECTION_ID&mapId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mapId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chicagoTransitAuthority/latest/actions/get-train-arrivals-by-station?${params}`, {
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
      "arrT": "2026-05-07T12:00:00.000Z",
      "destNm": "string",
      "destSt": "string",
      "heading": "string",
      "isApp": true,
      "isDly": true,
      "isFlt": true,
      "isSch": true,
      "lat": "string",
      "lon": "string",
      "prdt": "2026-05-07T12:00:00.000Z",
      "rn": "string",
      "rt": "string",
      "staId": "string",
      "staNm": "string",
      "stpDe": "string",
      "stpId": "string",
      "trDr": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Train Arrivals by Station action reference](actions/get-train-arrivals-by-station.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/chicagoTransitAuthority/latest/actions/get-train-arrivals-by-station).
