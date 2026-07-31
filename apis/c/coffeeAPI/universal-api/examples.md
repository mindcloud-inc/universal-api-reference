# Coffee API Universal API Examples

These examples use the MindCloud API key and Coffee API connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Random Coffee Image



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coffeeAPI/latest/actions/get-random-coffee-image?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coffeeAPI/latest/actions/get-random-coffee-image?${params}`, {
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

See the full [Get Random Coffee Image action reference](actions/get-random-coffee-image.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/coffeeAPI/latest/actions/get-random-coffee-image).
