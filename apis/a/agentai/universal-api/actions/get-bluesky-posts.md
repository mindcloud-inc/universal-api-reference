# Agent.ai: Get Bluesky Posts

Retrieves Bluesky posts from Agent.ai by handle.

```
GET https://connect.mindcloud.co/v1/universal/agentai/latest/actions/get-bluesky-posts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agent.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agentai/latest/actions/get-bluesky-posts?connectionId=$CONNECTION_ID&handle=string&numPosts=5" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "handle": "string",
  "numPosts": "5"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agentai/latest/actions/get-bluesky-posts?${params}`, {
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
| `handle` | string | yes | Bluesky handle to fetch posts from. |
| `numPosts` | number | yes | Number of Bluesky posts to fetch. Default: `5`. |

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
| `response` | array<object> | Retrieved Bluesky posts. |
| `status` | number | HTTP status code of the action response. |

## Native endpoint

Through the native Agent.ai API, this operation is `POST /action/get_bluesky_posts` (base URL `https://api-lr.agent.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bluesky-posts.md) for the provider-specific parameters and requirements.

