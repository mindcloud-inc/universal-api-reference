# PlaceBear Universal API Examples

These examples use the MindCloud API key and PlaceBear connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Bear Image



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/placeBear/latest/actions/get-bear-image?connectionId=$CONNECTION_ID&width=1&height=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "width": "1",
  "height": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/placeBear/latest/actions/get-bear-image?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [Get Bear Image action reference](actions/get-bear-image.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/placeBear/latest/actions/get-bear-image).
