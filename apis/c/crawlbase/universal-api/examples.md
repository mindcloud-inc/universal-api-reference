# Crawlbase Universal API Examples

These examples use the MindCloud API key and Crawlbase connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User Agents

Retrieves random user-agent strings from Crawlbase.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crawlbase/latest/actions/get-user-agents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crawlbase/latest/actions/get-user-agents?${params}`, {
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
      "agents": [
        "string"
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Get User Agents action reference](actions/get-user-agents.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/crawlbase/latest/actions/get-user-agents).
