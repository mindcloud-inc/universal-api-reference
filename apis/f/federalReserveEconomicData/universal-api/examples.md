# Federal Reserve Economic Data Universal API Examples

These examples use the MindCloud API key and Federal Reserve Economic Data connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Sources

Retrieves sources from Federal Reserve Economic Data.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/federalReserveEconomicData/latest/actions/list-sources?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/federalReserveEconomicData/latest/actions/list-sources?${params}`, {
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
      "count": 1,
      "limit": 1,
      "offset": 1,
      "order_by": "string",
      "realtime_end": "2026-05-07T12:00:00.000Z",
      "realtime_start": "2026-05-07T12:00:00.000Z",
      "sort_order": "string",
      "sources": [
        {
          "id": 1,
          "link": "https://example.com",
          "name": "Ava Chen",
          "realtime_end": "2026-05-07T12:00:00.000Z",
          "realtime_start": "2026-05-07T12:00:00.000Z"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Sources action reference](actions/list-sources.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/federalReserveEconomicData/latest/actions/list-sources).
