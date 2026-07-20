# Lex Fridman Podcast: Get OEmbed Namespace Info

Retrieves oEmbed namespace details from Lex Fridman Podcast.

```
GET https://connect.mindcloud.co/v1/universal/lexFridmanPodcast/latest/actions/get-oembed-namespace-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lex Fridman Podcast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lexFridmanPodcast/latest/actions/get-oembed-namespace-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lexFridmanPodcast/latest/actions/get-oembed-namespace-info?${params}`, {
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
      "namespace": "Ava Chen",
      "routes": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `namespace` | string |  |
| `routes` | object |  |

## Native endpoint

Through the native Lex Fridman Podcast API, this operation is `GET /wp-json/oembed/1.0` (base URL `https://lexfridman.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-oembed-namespace-info.md) for the provider-specific parameters and requirements.

