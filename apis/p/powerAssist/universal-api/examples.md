# Power Assist Universal API Examples

These examples use the MindCloud API key and Power Assist connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Clean Whitespace

Cleans whitespace in a string with Power Assist.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/powerAssist/latest/actions/clean-whitespace?connectionId=$CONNECTION_ID&string=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "string": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/powerAssist/latest/actions/clean-whitespace?${params}`, {
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
      "Result": "string"
    }
  ],
  "meta": {}
}
```

See the full [Clean Whitespace action reference](actions/clean-whitespace.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/powerAssist/latest/actions/clean-whitespace).
