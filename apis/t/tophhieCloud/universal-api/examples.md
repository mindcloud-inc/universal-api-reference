# Tophhie Cloud Universal API Examples

These examples use the MindCloud API key and Tophhie Cloud connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Check IP



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tophhieCloud/latest/actions/check-ip?connectionId=$CONNECTION_ID&ip=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ip": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tophhieCloud/latest/actions/check-ip?${params}`, {
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
      "ipVersion": 1,
      "mapsUrl": {},
      "metadata": {},
      "result": "string"
    }
  ],
  "meta": {}
}
```

See the full [Check IP action reference](actions/check-ip.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tophhieCloud/latest/actions/check-ip).
