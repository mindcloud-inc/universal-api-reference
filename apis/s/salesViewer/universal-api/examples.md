# SalesViewer Universal API Examples

These examples use the MindCloud API key and SalesViewer connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Search Sessions

Finds sessions in SalesViewer by query parameters.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesViewer/latest/actions/search-sessions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesViewer/latest/actions/search-sessions?${params}`, {
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
      "pagination": {
        "current": 1,
        "isFirst": true,
        "isLast": true,
        "pageSize": 1,
        "total": 1,
        "totalItems": 1
      },
      "result": [
        {}
      ],
      "totals": {
        "companies": 1,
        "interest_visits": 1,
        "interests": 1,
        "sessions": 1,
        "visits": 1
      }
    }
  ],
  "meta": {}
}
```

See the full [Search Sessions action reference](actions/search-sessions.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/salesViewer/latest/actions/search-sessions).
