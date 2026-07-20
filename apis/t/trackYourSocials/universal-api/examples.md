# TrackYourSocials Universal API Examples

These examples use the MindCloud API key and TrackYourSocials connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Post Analytics

Retrieves engagement metrics for a social media post from TrackYourSocials.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trackYourSocials/latest/actions/get-post-analytics?connectionId=$CONNECTION_ID&mediaLink=https%3A%2F%2Finstagram.com%2Fp%2FABC123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mediaLink": "https://instagram.com/p/ABC123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trackYourSocials/latest/actions/get-post-analytics?${params}`, {
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
      "comments": 1,
      "Likes": 1,
      "platform": "string",
      "post": "string",
      "success": true,
      "thumbnail": "string",
      "views": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Post Analytics action reference](actions/get-post-analytics.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/trackYourSocials/latest/actions/get-post-analytics).
