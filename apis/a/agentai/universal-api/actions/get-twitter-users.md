# Agent.ai: Get Twitter Users

Finds Twitter user profiles in Agent.ai by keywords.

```
GET https://connect.mindcloud.co/v1/universal/agentai/latest/actions/get-twitter-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agent.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agentai/latest/actions/get-twitter-users?connectionId=$CONNECTION_ID&keywords=string&numUsers=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "keywords": "string",
  "numUsers": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agentai/latest/actions/get-twitter-users?${params}`, {
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
| `keywords` | string | yes | Keywords to find relevant Twitter users. |
| `numUsers` | number | yes | Number of user profiles to retrieve. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": [
        "string"
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
| `response` | array<string> |  |
| `status` | number |  |

## Native endpoint

Through the native Agent.ai API, this operation is `POST /action/get_twitter_users` (base URL `https://api-lr.agent.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-twitter-users.md) for the provider-specific parameters and requirements.

