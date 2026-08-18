# Facebook Universal API Examples

These examples use the MindCloud API key and Facebook connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Ad Campaign Query



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/facebook/latest/actions/ad-campaign-query?connectionId=$CONNECTION_ID&accountID=act_112816323599903" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountID": "act_112816323599903"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/facebook/latest/actions/ad-campaign-query?${params}`, {
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

See the full [Ad Campaign Query action reference](actions/ad-campaign-query.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/facebook/latest/actions/ad-campaign-query).
