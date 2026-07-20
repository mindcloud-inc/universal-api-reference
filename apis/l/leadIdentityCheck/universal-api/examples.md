# Lead Identity Check Universal API Examples

These examples use the MindCloud API key and Lead Identity Check connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Authenticate Connection



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadIdentityCheck/latest/actions/authenticate-connection?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadIdentityCheck/latest/actions/authenticate-connection?${params}`, {
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
      "email": "ava@example.com"
    }
  ],
  "meta": {}
}
```

See the full [Authenticate Connection action reference](actions/authenticate-connection.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/leadIdentityCheck/latest/actions/authenticate-connection).
