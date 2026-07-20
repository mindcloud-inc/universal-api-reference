# Agent.ai: Get Search Results

Finds Google or YouTube results in Agent.ai by query.

```
GET https://connect.mindcloud.co/v1/universal/agentai/latest/actions/get-search-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agent.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agentai/latest/actions/get-search-results?connectionId=$CONNECTION_ID&searchEngine=google&query=string&numPosts=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "searchEngine": "google",
  "query": "string",
  "numPosts": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agentai/latest/actions/get-search-results?${params}`, {
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
| `searchEngine` | string | yes | Search engine to use. Default: `google`. |
| `query` | string | yes | Search terms to find specific results. |
| `numPosts` | number | yes | Number of results to return. Default: `1`. |

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
| `response` | object | Search results returned by Agent.ai. |
| `status` | number | HTTP status code of the action response. |

## Native endpoint

Through the native Agent.ai API, this operation is `POST /action/get_search_results` (base URL `https://api-lr.agent.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-search-results.md) for the provider-specific parameters and requirements.

