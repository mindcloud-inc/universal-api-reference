# Meme API: Fetch Random Memes



```
GET https://connect.mindcloud.co/v1/universal/memeAPI/latest/actions/fetch-random-memes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Meme API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/memeAPI/latest/actions/fetch-random-memes?connectionId=$CONNECTION_ID&count=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "count": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/memeAPI/latest/actions/fetch-random-memes?${params}`, {
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
| `count` | number | yes | Required meme count (1-50). |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `memes` | array<object> |  |

## Native endpoint

Through the native Meme API API, this operation is `GET /gimme/:count` (base URL `https://meme-api.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-random-memes.md) for the provider-specific parameters and requirements.

