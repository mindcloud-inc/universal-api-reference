# Planerka Universal API Examples

These examples use the MindCloud API key and Planerka connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get API status

Retrieves API status from Planerka.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/planerka/latest/actions/get-api-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/planerka/latest/actions/get-api-status?${params}`, {
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

See the full [Get API status action reference](actions/get-api-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/planerka/latest/actions/get-api-status).
