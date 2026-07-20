# Sigma Universal API Examples

These examples use the MindCloud API key and Sigma connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Connections



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sigma/latest/actions/list-connections?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sigma/latest/actions/list-connections?${params}`, {
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
      "entries": [
        {}
      ],
      "hasMore": true,
      "nextPage": "string",
      "total": 1
    }
  ],
  "meta": {}
}
```

See the full [List Connections action reference](actions/list-connections.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sigma/latest/actions/list-connections).
