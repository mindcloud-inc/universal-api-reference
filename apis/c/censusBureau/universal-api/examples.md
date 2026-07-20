# Census Bureau Universal API Examples

These examples use the MindCloud API key and Census Bureau connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Query 2024 ACS 1-Year Detailed Tables

Queries Census Bureau 2024 ACS 1-Year detailed tables.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/censusBureau/latest/actions/query2024-acs1-detailed-tables?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/censusBureau/latest/actions/query2024-acs1-detailed-tables?${params}`, {
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

See the full [Query 2024 ACS 1-Year Detailed Tables action reference](actions/query2024-acs1-detailed-tables.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/censusBureau/latest/actions/query2024-acs1-detailed-tables).
