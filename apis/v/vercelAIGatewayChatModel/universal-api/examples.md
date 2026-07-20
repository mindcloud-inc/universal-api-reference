# Vercel AI Gateway Chat Model Universal API Examples

These examples use the MindCloud API key and Vercel AI Gateway Chat Model connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Credits

Retrieves AI Gateway credit balance and spend from Vercel.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vercelAIGatewayChatModel/latest/actions/get-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vercelAIGatewayChatModel/latest/actions/get-credits?${params}`, {
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
      "balance": 1,
      "totalUsed": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Credits action reference](actions/get-credits.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/vercelAIGatewayChatModel/latest/actions/get-credits).
