# Meow Facts Universal API Examples

These examples use the MindCloud API key and Meow Facts connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get cat facts



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/meowFacts/latest/actions/get-cat-facts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/meowFacts/latest/actions/get-cat-facts?${params}`, {
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
      "data": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [Get cat facts action reference](actions/get-cat-facts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/meowFacts/latest/actions/get-cat-facts).
