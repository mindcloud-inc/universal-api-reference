# Insult API Universal API Examples

These examples use the MindCloud API key and Insult API connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Adjective



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/insultAPI/latest/actions/get-adjective?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/insultAPI/latest/actions/get-adjective?${params}`, {
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

See the full [Get Adjective action reference](actions/get-adjective.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/insultAPI/latest/actions/get-adjective).
