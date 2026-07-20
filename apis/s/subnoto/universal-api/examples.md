# Subnoto Universal API Examples

These examples use the MindCloud API key and Subnoto connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Who Am I



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/subnoto/latest/actions/who-am-i?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/subnoto/latest/actions/who-am-i?${params}`, {
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
      "accessKey": "string",
      "agent": {},
      "ownerEmail": "ava@example.com",
      "ownerUuid": "string",
      "teamName": "Ava Chen",
      "teamUuid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Who Am I action reference](actions/who-am-i.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/subnoto/latest/actions/who-am-i).
