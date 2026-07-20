# Agent.ai: Get Instagram Followers

Retrieves Instagram followers from Agent.ai by username.

```
GET https://connect.mindcloud.co/v1/universal/agentai/latest/actions/get-instagram-followers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agent.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agentai/latest/actions/get-instagram-followers?connectionId=$CONNECTION_ID&username=Ava%20Chen&limit=20" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "username": "Ava Chen",
  "limit": "20"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agentai/latest/actions/get-instagram-followers?${params}`, {
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
| `username` | string | yes | Instagram username without @. |
| `limit` | string | yes | Number of top followers to retrieve. Default: `20`. |

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
| `response` | array<object> | Instagram followers returned by the action. |
| `status` | number | HTTP status code of the action response. |

## Native endpoint

Through the native Agent.ai API, this operation is `POST /action/get_instagram_followers` (base URL `https://api-lr.agent.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-instagram-followers.md) for the provider-specific parameters and requirements.

