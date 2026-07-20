# Talk Python To Me: Search Episodes and Transcripts

Finds episodes and transcripts in Talk Python To Me.

```
GET https://connect.mindcloud.co/v1/universal/talkPythonToMe/latest/actions/search-episodes-and-transcripts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Talk Python To Me `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/talkPythonToMe/latest/actions/search-episodes-and-transcripts?connectionId=$CONNECTION_ID&query=python-testing" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "python-testing"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/talkPythonToMe/latest/actions/search-episodes-and-transcripts?${params}`, {
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
| `query` | string | yes | Search text to look for in Talk Python episodes and transcript content. Use hyphen-separated words for multi-keyword searches, such as python-testing. Example: `python-testing`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "description": "string",
      "id": 1,
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string | Result type returned by the search API, such as Episode. |
| `description` | string | Search result summary or transcript excerpt text. |
| `id` | number | Talk Python episode identifier. |
| `title` | string | Search result title. |
| `url` | string | Relative Talk Python URL for the result. |

## Native endpoint

Through the native Talk Python To Me API, this operation is `GET /search` (base URL `https://search.talkpython.fm/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-episodes-and-transcripts.md) for the provider-specific parameters and requirements.

