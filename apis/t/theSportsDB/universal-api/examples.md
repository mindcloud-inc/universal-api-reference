# TheSportsDB Universal API Examples

These examples use the MindCloud API key and TheSportsDB connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List All Sports

Retrieves all sport categories from TheSportsDB.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/theSportsDB/latest/actions/list-all-sports?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/theSportsDB/latest/actions/list-all-sports?${params}`, {
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
      "sports": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [List All Sports action reference](actions/list-all-sports.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/theSportsDB/latest/actions/list-all-sports).
