# SHOUTCLOUD Universal API Examples

These examples use the MindCloud API key and SHOUTCLOUD connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Shout Text



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sHOUTCLOUD/latest/actions/shout-text?connectionId=$CONNECTION_ID&INPUT=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "INPUT": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sHOUTCLOUD/latest/actions/shout-text?${params}`, {
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
      "OUTPUT": "string"
    }
  ],
  "meta": {}
}
```

See the full [Shout Text action reference](actions/shout-text.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sHOUTCLOUD/latest/actions/shout-text).
