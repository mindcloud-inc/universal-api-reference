# DailyMed Universal API Examples

These examples use the MindCloud API key and DailyMed connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List SPLs

Retrieves SPLs from DailyMed.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dailyMed/latest/actions/list-spls?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dailyMed/latest/actions/list-spls?${params}`, {
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
      "published_date": "2026-05-07T12:00:00.000Z",
      "setid": "string",
      "spl_version": 1,
      "title": "string"
    }
  ],
  "meta": {}
}
```

See the full [List SPLs action reference](actions/list-spls.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dailyMed/latest/actions/list-spls).
