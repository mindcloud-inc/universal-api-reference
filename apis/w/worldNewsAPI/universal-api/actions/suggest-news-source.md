# World News API: Suggest News Source

Creates a news source suggestion in World News API.

```
POST https://connect.mindcloud.co/v1/universal/worldNewsAPI/latest/actions/suggest-news-source
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a World News API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/worldNewsAPI/latest/actions/suggest-news-source" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://www.cnn.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/worldNewsAPI/latest/actions/suggest-news-source', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://www.cnn.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `feedUrl` | string | no | Optional RSS or Atom feed URL for the suggested news source. |
| `url` | string | yes | News source website URL to suggest for monitoring. Default: `https://www.cnn.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Provider acknowledgement for the suggested news source. |

## Native endpoint

Through the native World News API API, this operation is `POST /suggest-news-source` (base URL `https://api.worldnewsapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/suggest-news-source.md) for the provider-specific parameters and requirements.

