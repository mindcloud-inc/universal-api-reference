# Meme API Universal API Examples

These examples use the MindCloud API key and Meme API connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Fetch Memes From Subreddit



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/memeAPI/latest/actions/fetch-memes-from-subreddit?connectionId=$CONNECTION_ID&subreddit=string&count=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "subreddit": "string",
  "count": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/memeAPI/latest/actions/fetch-memes-from-subreddit?${params}`, {
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
      "count": 1,
      "memes": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Fetch Memes From Subreddit action reference](actions/fetch-memes-from-subreddit.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/memeAPI/latest/actions/fetch-memes-from-subreddit).
