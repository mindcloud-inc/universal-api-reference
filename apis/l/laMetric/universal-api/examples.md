# LaMetric Universal API Examples

These examples use the MindCloud API key and LaMetric connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Devices

Retrieves devices from LaMetric.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/laMetric/latest/actions/list-devices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/laMetric/latest/actions/list-devices?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [List Devices action reference](actions/list-devices.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/laMetric/latest/actions/list-devices).
