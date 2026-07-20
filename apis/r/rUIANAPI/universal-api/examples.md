# RUIAN Universal API Examples

These examples use the MindCloud API key and RUIAN connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get all layers and tables

Retrieves layers and tables from RUIAN API.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rUIANAPI/latest/actions/get-all-layers-and-tables?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rUIANAPI/latest/actions/get-all-layers-and-tables?${params}`, {
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
      "layers": [
        {}
      ],
      "tables": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Get all layers and tables action reference](actions/get-all-layers-and-tables.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rUIANAPI/latest/actions/get-all-layers-and-tables).
