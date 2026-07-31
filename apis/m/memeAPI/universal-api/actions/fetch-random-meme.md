# Meme API: Fetch Random Meme



```
GET https://connect.mindcloud.co/v1/universal/memeAPI/latest/actions/fetch-random-meme
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Meme API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/memeAPI/latest/actions/fetch-random-meme?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/memeAPI/latest/actions/fetch-random-meme?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "author": "string",
      "nsfw": true,
      "postLink": "https://example.com",
      "spoiler": true,
      "subreddit": "string",
      "title": "string",
      "ups": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | string |  |
| `nsfw` | boolean |  |
| `postLink` | string |  |
| `spoiler` | boolean |  |
| `subreddit` | string |  |
| `title` | string |  |
| `ups` | number |  |
| `url` | string |  |

## Native endpoint

Through the native Meme API API, this operation is `GET /gimme` (base URL `https://meme-api.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-random-meme.md) for the provider-specific parameters and requirements.

