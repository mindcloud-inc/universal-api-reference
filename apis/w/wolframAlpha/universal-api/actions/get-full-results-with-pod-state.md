# Wolfram Alpha: Get Full Results with Pod State

Retrieves full Wolfram Alpha query results with a pod state.

```
GET https://connect.mindcloud.co/v1/universal/wolframAlpha/latest/actions/get-full-results-with-pod-state
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wolfram Alpha `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wolframAlpha/latest/actions/get-full-results-with-pod-state?connectionId=$CONNECTION_ID&input=string&podstate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "input": "string",
  "podstate": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wolframAlpha/latest/actions/get-full-results-with-pod-state?${params}`, {
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
| `input` | string | yes |  |
| `podstate` | string | yes |  |

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

Through the native Wolfram Alpha API, this operation is `GET /v2/query` (base URL `https://api.wolframalpha.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-full-results-with-pod-state.md) for the provider-specific parameters and requirements.

