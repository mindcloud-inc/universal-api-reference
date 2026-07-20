# NewsData.io Universal API Examples

These examples use the MindCloud API key and NewsData.io connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Latest News



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/newsDataio/latest/actions/list-latest-news?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/newsDataio/latest/actions/list-latest-news?${params}`, {
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
      "nextPage": "string",
      "results": [
        {}
      ],
      "status": "string",
      "totalResults": 1
    }
  ],
  "meta": {}
}
```

See the full [List Latest News action reference](actions/list-latest-news.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/newsDataio/latest/actions/list-latest-news).
