# Basalt Universal API Examples

These examples use the MindCloud API key and Basalt connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Prompts

Retrieves a list of prompts from Basalt.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/basalt/latest/actions/list-prompts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/basalt/latest/actions/list-prompts?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [List Prompts action reference](actions/list-prompts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/basalt/latest/actions/list-prompts).
