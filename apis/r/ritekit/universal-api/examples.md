# Ritekit Universal API Examples

These examples use the MindCloud API key and Ritekit connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Trending Hashtags

Retrieves trending hashtags from Ritekit.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ritekit/latest/actions/list-trending-hashtags?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ritekit/latest/actions/list-trending-hashtags?${params}`, {
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
      "code": 1,
      "message": "string",
      "result": true,
      "tags": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Trending Hashtags action reference](actions/list-trending-hashtags.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ritekit/latest/actions/list-trending-hashtags).
