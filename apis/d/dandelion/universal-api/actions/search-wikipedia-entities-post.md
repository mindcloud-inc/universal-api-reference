# Dandelion: Search Wikipedia Entities via HTTP POST

Searches Wikipedia entities in Dandelion via HTTP POST.

```
GET https://connect.mindcloud.co/v1/universal/dandelion/latest/actions/search-wikipedia-entities-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dandelion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dandelion/latest/actions/search-wikipedia-entities-post?connectionId=$CONNECTION_ID&text=string&lang=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "text": "string",
  "lang": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dandelion/latest/actions/search-wikipedia-entities-post?${params}`, {
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
| `text` | string | yes | Search text to match against Wikipedia. |
| `lang` | string | yes | Language of the input text. |
| `limit` | number | no | Restrict results to the first N matches. |
| `offset` | number | no | Start listing results from this index. |
| `include` | string | no | Comma-separated list of extra entity fields to include. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "entities": [
        {}
      ],
      "lang": "string",
      "query": "string",
      "time": 1,
      "timestamp": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `entities` | array<object> |  |
| `lang` | string |  |
| `query` | string |  |
| `time` | number |  |
| `timestamp` | string |  |

## Native endpoint

Through the native Dandelion API, this operation is `POST /datagraph/wikisearch/v1` (base URL `https://api.dandelion.eu`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-wikipedia-entities-post.md) for the provider-specific parameters and requirements.

