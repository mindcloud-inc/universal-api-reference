# Dog Facts Universal API Examples

These examples use the MindCloud API key and Dog Facts connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Dog Facts



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dogFacts/latest/actions/list-dog-facts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dogFacts/latest/actions/list-dog-facts?${params}`, {
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
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Dog Facts action reference](actions/list-dog-facts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dogFacts/latest/actions/list-dog-facts).
