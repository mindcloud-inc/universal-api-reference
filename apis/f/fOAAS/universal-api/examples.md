# FOAAS Universal API Examples

These examples use the MindCloud API key and FOAAS connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Asshole



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fOAAS/latest/actions/asshole?connectionId=$CONNECTION_ID&from=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "from": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fOAAS/latest/actions/asshole?${params}`, {
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
      "message": "string",
      "subtitle": "string"
    }
  ],
  "meta": {}
}
```

See the full [Asshole action reference](actions/asshole.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fOAAS/latest/actions/asshole).
