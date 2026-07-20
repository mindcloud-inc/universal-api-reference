# icanhazdadjoke Universal API Examples

These examples use the MindCloud API key and icanhazdadjoke connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Fetch Dad Joke

Retrieves a specific dad joke from icanhazdadjoke.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/icanhazdadjoke/latest/actions/fetch-dad-joke?connectionId=$CONNECTION_ID&jokeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jokeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/icanhazdadjoke/latest/actions/fetch-dad-joke?${params}`, {
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
      "id": "string",
      "joke": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

See the full [Fetch Dad Joke action reference](actions/fetch-dad-joke.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/icanhazdadjoke/latest/actions/fetch-dad-joke).
