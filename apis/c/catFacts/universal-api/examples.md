# Cat Facts Universal API Examples

These examples use the MindCloud API key and Cat Facts connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Random Fact



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/catFacts/latest/actions/get-random-fact?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/catFacts/latest/actions/get-random-fact?${params}`, {
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
      "fact": "string",
      "length": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Random Fact action reference](actions/get-random-fact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/catFacts/latest/actions/get-random-fact).
