# Chuck Norris Universal API Examples

These examples use the MindCloud API key and Chuck Norris connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Random Fact



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chuckNorris/latest/actions/get-random-fact?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chuckNorris/latest/actions/get-random-fact?${params}`, {
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
      "categories": [
        "string"
      ],
      "created_at": "string",
      "icon_url": "https://example.com",
      "id": "string",
      "updated_at": "string",
      "url": "https://example.com",
      "value": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Random Fact action reference](actions/get-random-fact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/chuckNorris/latest/actions/get-random-fact).
