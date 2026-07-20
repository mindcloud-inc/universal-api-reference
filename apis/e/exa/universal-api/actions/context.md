# Exa: Context

Retrieves context from Exa.

```
GET https://connect.mindcloud.co/v1/universal/exa/latest/actions/context
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Exa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/exa/latest/actions/context?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/exa/latest/actions/context?${params}`, {
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
| `query` | string | yes | Search query to find relevant code context. |
| `tokensNum` | number | no | Token budget for the response. Use a number or dynamic. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "costDollars": "string",
      "outputTokens": 1,
      "query": "string",
      "requestId": "string",
      "response": "string",
      "resultsCount": 1,
      "searchTime": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `costDollars` | string |  |
| `outputTokens` | number |  |
| `query` | string |  |
| `requestId` | string |  |
| `response` | string |  |
| `resultsCount` | number |  |
| `searchTime` | number |  |

## Native endpoint

Through the native Exa API, this operation is `POST /context` (base URL `https://api.exa.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/context.md) for the provider-specific parameters and requirements.

