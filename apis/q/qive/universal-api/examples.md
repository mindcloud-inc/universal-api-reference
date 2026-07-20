# Qive Universal API Examples

These examples use the MindCloud API key and Qive connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Companies



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qive/latest/actions/get-companies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qive/latest/actions/get-companies?${params}`, {
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

See the full [Get Companies action reference](actions/get-companies.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/qive/latest/actions/get-companies).
