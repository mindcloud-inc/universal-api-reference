# Wolfram Alpha: Follow Async Pod URL

Retrieves an asynchronous pod result from Wolfram Alpha.

```
GET https://connect.mindcloud.co/v1/universal/wolframAlpha/latest/actions/follow-async-pod-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wolfram Alpha `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wolframAlpha/latest/actions/follow-async-pod-url?connectionId=$CONNECTION_ID&asyncPodUrl=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "asyncPodUrl": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wolframAlpha/latest/actions/follow-async-pod-url?${params}`, {
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
| `asyncPodUrl` | string | yes | Full async pod URL returned by a prior Full Results response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "inputString": "string",
      "podCount": 1,
      "primaryResult": "string",
      "query": "string",
      "resultId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `inputString` | string | Normalized query input string. |
| `podCount` | number | Number of pods returned. |
| `primaryResult` | string | Primary result text when available. |
| `query` | string | Original query text. |
| `resultId` | string | Result identifier. |

## Native endpoint

Through the native Wolfram Alpha API, this operation is `GET {{asyncPodUrl}}` (base URL `https://api.wolframalpha.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/follow-async-pod-url.md) for the provider-specific parameters and requirements.

