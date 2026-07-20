# OpenRegister Universal API Examples

These examples use the MindCloud API key and OpenRegister connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Advanced Company Search

Finds companies in OpenRegister using advanced filters.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openRegister/latest/actions/advanced-company-search?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openRegister/latest/actions/advanced-company-search?${params}`, {
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
      "pagination": {},
      "results": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Advanced Company Search action reference](actions/advanced-company-search.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/openRegister/latest/actions/advanced-company-search).
