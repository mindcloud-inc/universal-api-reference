# NioLeads Universal API Examples

These examples use the MindCloud API key and NioLeads connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Credits

Retrieves your available credit balance from NioLeads.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nioLeads/latest/actions/get-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nioLeads/latest/actions/get-credits?${params}`, {
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
      "totalCredits": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Credits action reference](actions/get-credits.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/nioLeads/latest/actions/get-credits).
