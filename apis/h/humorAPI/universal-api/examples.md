# Humor API Universal API Examples

These examples use the MindCloud API key and Humor API connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Random Joke



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/humorAPI/latest/actions/get-random-joke?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/humorAPI/latest/actions/get-random-joke?${params}`, {
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
      "joke": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Random Joke action reference](actions/get-random-joke.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/humorAPI/latest/actions/get-random-joke).

## Create Joke



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/humorAPI/latest/actions/create-joke" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/humorAPI/latest/actions/create-joke', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "joke": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Joke action reference](actions/create-joke.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/humorAPI/latest/actions/create-joke).
