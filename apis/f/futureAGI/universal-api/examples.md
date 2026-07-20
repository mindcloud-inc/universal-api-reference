# FutureAGI Universal API Examples

These examples use the MindCloud API key and FutureAGI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Agent Definitions



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/futureAGI/latest/actions/list-agent-definitions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/futureAGI/latest/actions/list-agent-definitions?${params}`, {
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
      "count": 1,
      "currentPage": 1,
      "next": "string",
      "previous": "string",
      "results": [
        {}
      ],
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

See the full [List Agent Definitions action reference](actions/list-agent-definitions.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/futureAGI/latest/actions/list-agent-definitions).
