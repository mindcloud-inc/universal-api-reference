# Bacon Ipsum Universal API Examples

These examples use the MindCloud API key and Bacon Ipsum connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Generate Bacon Ipsum



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/baconIpsum/latest/actions/generate-bacon-ipsum?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/baconIpsum/latest/actions/generate-bacon-ipsum?${params}`, {
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
    {}
  ],
  "meta": {}
}
```

See the full [Generate Bacon Ipsum action reference](actions/generate-bacon-ipsum.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/baconIpsum/latest/actions/generate-bacon-ipsum).
