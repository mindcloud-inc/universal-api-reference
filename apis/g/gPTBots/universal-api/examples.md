# GPTBots Universal API Examples

These examples use the MindCloud API key and GPTBots connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Agent Information

Retrieves the configured agent information from GPTBots.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gPTBots/latest/actions/get-agent-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gPTBots/latest/actions/get-agent-information?${params}`, {
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

See the full [Get Agent Information action reference](actions/get-agent-information.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/gPTBots/latest/actions/get-agent-information).
