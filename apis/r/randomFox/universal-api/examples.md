# RandomFox Universal API Examples

These examples use the MindCloud API key and RandomFox connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Random Fox



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/randomFox/latest/actions/get-random-fox?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/randomFox/latest/actions/get-random-fox?${params}`, {
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
      "image": "string",
      "link": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Get Random Fox action reference](actions/get-random-fox.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/randomFox/latest/actions/get-random-fox).
