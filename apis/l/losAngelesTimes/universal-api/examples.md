# Los Angeles Times Universal API Examples

These examples use the MindCloud API key and Los Angeles Times connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Business Stories

Retrieves Los Angeles Times business stories.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/losAngelesTimes/latest/actions/list-business-stories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/losAngelesTimes/latest/actions/list-business-stories?${params}`, {
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
      "content:encoded": {},
      "dc:creator": "string",
      "description": {},
      "guid": "string",
      "link": "https://example.com",
      "media:content": {},
      "pubDate": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Business Stories action reference](actions/list-business-stories.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/losAngelesTimes/latest/actions/list-business-stories).
