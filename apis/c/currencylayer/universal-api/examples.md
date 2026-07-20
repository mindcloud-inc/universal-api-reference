# Currencylayer Universal API Examples

These examples use the MindCloud API key and Currencylayer connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Supported Currencies

Retrieves supported currencies from Currencylayer.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/currencylayer/latest/actions/list-supported-currencies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/currencylayer/latest/actions/list-supported-currencies?${params}`, {
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

See the full [List Supported Currencies action reference](actions/list-supported-currencies.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/currencylayer/latest/actions/list-supported-currencies).
