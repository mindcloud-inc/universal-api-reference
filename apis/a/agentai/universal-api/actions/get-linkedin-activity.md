# Agent.ai: Get LinkedIn Activity

Retrieves LinkedIn posts from Agent.ai by profile URL.

```
GET https://connect.mindcloud.co/v1/universal/agentai/latest/actions/get-linkedin-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agent.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agentai/latest/actions/get-linkedin-activity?connectionId=$CONNECTION_ID&profileUrls=https%3A%2F%2Fexample.com&numPosts=3" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "profileUrls": "https://example.com",
  "numPosts": "3"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agentai/latest/actions/get-linkedin-activity?${params}`, {
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
| `profileUrls` | string | yes | LinkedIn profile URLs, one per line. |
| `numPosts` | number | yes | Number of recent posts to fetch from each profile. Default: `3`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": {},
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | object | LinkedIn activity data. |
| `status` | number | HTTP status code of the action response. |

## Native endpoint

Through the native Agent.ai API, this operation is `POST /action/get_linkedin_activity` (base URL `https://api-lr.agent.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-linkedin-activity.md) for the provider-specific parameters and requirements.

