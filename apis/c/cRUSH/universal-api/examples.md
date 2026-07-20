# CRUSH Universal API Examples

These examples use the MindCloud API key and CRUSH connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List API Tokens



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cRUSH/latest/actions/list-api-tokens?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cRUSH/latest/actions/list-api-tokens?${params}`, {
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
      "key": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "isRevoked": true,
        "lastUsedAt": "2026-05-07T12:00:00.000Z",
        "requestCount": 1,
        "tokenPrefix": "string",
        "userId": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [List API Tokens action reference](actions/list-api-tokens.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cRUSH/latest/actions/list-api-tokens).
