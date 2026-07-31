# Official Joke API Universal API Examples

These examples use the MindCloud API key and Official Joke API connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Joke by ID



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/officialJokeAPI/latest/actions/get-joke-by-id?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/officialJokeAPI/latest/actions/get-joke-by-id?${params}`, {
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
      "id": 1,
      "punchline": "string",
      "setup": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Joke by ID action reference](actions/get-joke-by-id.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/officialJokeAPI/latest/actions/get-joke-by-id).
