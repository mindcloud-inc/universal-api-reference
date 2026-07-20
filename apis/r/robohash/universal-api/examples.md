# Robohash Universal API Examples

These examples use the MindCloud API key and Robohash connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Generate Image



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/robohash/latest/actions/generate-image?connectionId=$CONNECTION_ID&text=user%40example.com&format=png" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "text": "user@example.com",
  "format": "png"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/robohash/latest/actions/generate-image?${params}`, {
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
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Generate Image action reference](actions/generate-image.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/robohash/latest/actions/generate-image).
