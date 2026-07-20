# Agent.ai: Search Bluesky Posts

Finds Bluesky posts in Agent.ai by query.

```
GET https://connect.mindcloud.co/v1/universal/agentai/latest/actions/search-bluesky-posts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agent.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agentai/latest/actions/search-bluesky-posts?connectionId=$CONNECTION_ID&query=string&numPosts=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string",
  "numPosts": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agentai/latest/actions/search-bluesky-posts?${params}`, {
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
| `query` | string | yes | Text query to search Bluesky posts. |
| `numPosts` | number | yes | Number of Bluesky posts to return. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": [
        {}
      ],
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | array<object> | Bluesky post search results. |
| `status` | number | HTTP status code of the action response. |

## Native endpoint

Through the native Agent.ai API, this operation is `POST /action/search_bluesky_posts` (base URL `https://api-lr.agent.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-bluesky-posts.md) for the provider-specific parameters and requirements.

