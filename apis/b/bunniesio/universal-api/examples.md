# Bunnies.io Universal API Examples

These examples use the MindCloud API key and Bunnies.io connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Random Bunny



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bunniesio/latest/actions/get-random-bunny?connectionId=$CONNECTION_ID&media=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "media": "0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bunniesio/latest/actions/get-random-bunny?${params}`, {
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
      "id": "string",
      "media": {},
      "source": "string",
      "thisServed": 1,
      "totalServed": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Random Bunny action reference](actions/get-random-bunny.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bunniesio/latest/actions/get-random-bunny).
