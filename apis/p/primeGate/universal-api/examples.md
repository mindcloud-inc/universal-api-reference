# PrimeGate Universal API Examples

These examples use the MindCloud API key and PrimeGate connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Leads



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/primeGate/latest/actions/list-leads?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/primeGate/latest/actions/list-leads?${params}`, {
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

See the full [List Leads action reference](actions/list-leads.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/primeGate/latest/actions/list-leads).
