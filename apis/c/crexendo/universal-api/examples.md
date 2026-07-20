# Crexendo Universal API Examples

These examples use the MindCloud API key and Crexendo connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Domains

Retrieves domains from Crexendo.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crexendo/latest/actions/list-domains?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crexendo/latest/actions/list-domains?${params}`, {
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
      "count-users-configured": 1,
      "description": "string",
      "domain": "string",
      "domain-type": "string",
      "reseller": "string",
      "time-zone": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Domains action reference](actions/list-domains.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/crexendo/latest/actions/list-domains).
