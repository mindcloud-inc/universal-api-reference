# Epion Universal API Examples

These examples use the MindCloud API key and Epion connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Current Measurements

Retrieves current device measurements from Epion.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/epion/latest/actions/list-current-measurements?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/epion/latest/actions/list-current-measurements?${params}`, {
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
      "co2": 1,
      "deviceId": "string",
      "deviceName": "Ava Chen",
      "fwVersion": "string",
      "humidity": 1,
      "pressure": 1,
      "temperature": 1
    }
  ],
  "meta": {}
}
```

See the full [List Current Measurements action reference](actions/list-current-measurements.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/epion/latest/actions/list-current-measurements).
