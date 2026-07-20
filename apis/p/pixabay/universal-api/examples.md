# Pixabay Universal API Examples

These examples use the MindCloud API key and Pixabay connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Search Images

Finds images in Pixabay.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pixabay/latest/actions/search-images?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pixabay/latest/actions/search-images?${params}`, {
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
      "hits": [
        {}
      ],
      "total": 1,
      "totalHits": 1
    }
  ],
  "meta": {}
}
```

See the full [Search Images action reference](actions/search-images.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pixabay/latest/actions/search-images).
