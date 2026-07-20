# Perplexity: List Async Chat Completions

Retrieves async chat completions from Perplexity.

```
GET https://connect.mindcloud.co/v1/universal/perplexity/latest/actions/list-async-chat-completions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Perplexity `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/perplexity/latest/actions/list-async-chat-completions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/perplexity/latest/actions/list-async-chat-completions?${params}`, {
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
      "next_token": "string",
      "requests": [
        {
          "completed_at": 1,
          "created_at": 1,
          "failed_at": 1,
          "id": "string",
          "model": "string",
          "started_at": 1,
          "status": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `next_token` | string |  |
| `requests[].completed_at` | number |  |
| `requests[].created_at` | number |  |
| `requests[].failed_at` | number |  |
| `requests[].id` | string |  |
| `requests[].model` | string |  |
| `requests[].started_at` | number |  |
| `requests[].status` | string |  |

## Native endpoint

Through the native Perplexity API, this operation is `GET /v1/async/sonar` (base URL `https://api.perplexity.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-async-chat-completions.md) for the provider-specific parameters and requirements.

