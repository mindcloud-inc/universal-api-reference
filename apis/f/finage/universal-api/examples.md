# Finage Universal API Examples

These examples use the MindCloud API key and Finage connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Market Status

Retrieves market status from Finage.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finage/latest/actions/get-market-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finage/latest/actions/get-market-status?${params}`, {
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

See the full [Get Market Status action reference](actions/get-market-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/finage/latest/actions/get-market-status).
