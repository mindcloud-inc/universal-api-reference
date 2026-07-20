# Feishu Base Universal API Examples

These examples use the MindCloud API key and Feishu Base connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get App Info

Retrieves metadata for a Feishu Base app.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/feishuBase/latest/actions/get-app-info?connectionId=$CONNECTION_ID&appToken=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appToken": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/feishuBase/latest/actions/get-app-info?${params}`, {
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
      "code": 1,
      "data": {},
      "msg": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get App Info action reference](actions/get-app-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/feishuBase/latest/actions/get-app-info).
