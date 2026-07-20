# Agent.ai: Get Recent Tweets

Retrieves recent tweets from Agent.ai by Twitter handle.

```
GET https://connect.mindcloud.co/v1/universal/agentai/latest/actions/get-recent-tweets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agent.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agentai/latest/actions/get-recent-tweets?connectionId=$CONNECTION_ID&profileHandle=string&recentTweetsCount=10" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "profileHandle": "string",
  "recentTweetsCount": "10"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agentai/latest/actions/get-recent-tweets?${params}`, {
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
| `profileHandle` | string | yes | Twitter handle to fetch recent tweets from. |
| `recentTweetsCount` | string | yes | Number of recent tweets to fetch. Default: `10`. |

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
| `response` | array<object> | Recent tweets from the specified handle. |
| `status` | number | HTTP status code of the action response. |

## Native endpoint

Through the native Agent.ai API, this operation is `POST /action/get_recent_tweets` (base URL `https://api-lr.agent.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-recent-tweets.md) for the provider-specific parameters and requirements.

