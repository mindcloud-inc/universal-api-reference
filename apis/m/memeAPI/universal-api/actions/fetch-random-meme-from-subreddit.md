# Meme API: Fetch Random Meme From Subreddit



```
GET https://connect.mindcloud.co/v1/universal/memeAPI/latest/actions/fetch-random-meme-from-subreddit
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Meme API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/memeAPI/latest/actions/fetch-random-meme-from-subreddit?connectionId=$CONNECTION_ID&subreddit=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "subreddit": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/memeAPI/latest/actions/fetch-random-meme-from-subreddit?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subreddit` | string | yes | Required subreddit name. |

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

Through the native Meme API API, this operation is `GET /gimme/:subreddit` (base URL `https://meme-api.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-random-meme-from-subreddit.md) for the provider-specific parameters and requirements.

