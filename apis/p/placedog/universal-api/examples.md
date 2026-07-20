# Placedog Universal API Examples

These examples use the MindCloud API key and Placedog connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Images

Retrieves available Placedog image IDs and attribution details.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/placedog/latest/actions/list-images?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/placedog/latest/actions/list-images?${params}`, {
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
      "attributionName": "Ava Chen",
      "attributionUrl": "https://example.com",
      "id": 1,
      "placeholderUrl": "https://example.com",
      "sampleImageUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Images action reference](actions/list-images.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/placedog/latest/actions/list-images).
