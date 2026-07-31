# random.dog Universal API Examples

These examples use the MindCloud API key and random.dog connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Random Dog Media



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/randomdog/latest/actions/get-random-dog-media?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/randomdog/latest/actions/get-random-dog-media?${params}`, {
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
      "fileSizeBytes": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Get Random Dog Media action reference](actions/get-random-dog-media.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/randomdog/latest/actions/get-random-dog-media).
