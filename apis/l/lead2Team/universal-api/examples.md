# Lead2Team Universal API Examples

These examples use the MindCloud API key and Lead2Team connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Widget ID



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lead2Team/latest/actions/get-widget-id?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lead2Team/latest/actions/get-widget-id?${params}`, {
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
      "key": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Widget ID action reference](actions/get-widget-id.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/lead2Team/latest/actions/get-widget-id).
