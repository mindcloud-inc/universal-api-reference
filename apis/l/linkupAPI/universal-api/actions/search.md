# LinkupAPI: Search

Finds web content in LinkupAPI by query.

```
GET https://connect.mindcloud.co/v1/universal/linkupAPI/latest/actions/search
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LinkupAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkupAPI/latest/actions/search?connectionId=$CONNECTION_ID&q=string&depth=0&outputType=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "string",
  "depth": "0",
  "outputType": "0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linkupAPI/latest/actions/search?${params}`, {
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
| `q` | string | yes | The natural-language question to search for. |
| `depth` | string | yes | How deeply Linkup should search for results. One of: `0`, `1`, `2`. |
| `outputType` | string | yes | The response format to return from Linkup search. One of: `0`, `1`, `2`. |
| `maxResults` | number | no | Maximum number of results to return. |
| `includeImages` | boolean | no | Include image results in the response. Default: `false`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fromDate` | date | no | Only consider results on or after this ISO date. |
| `toDate` | date | no | Only consider results on or before this ISO date. |
| `includeDomains[]` | array<string> | no | Restrict search results to these domains. |
| `excludeDomains[]` | array<string> | no | Exclude results from these domains. |
| `includeInlineCitations` | boolean | no | Include inline citations when the output type is sourcedAnswer. Default: `false`. |
| `structuredOutputSchema` | string | no | A JSON schema string describing the structured output to return when output type is structured. |
| `includeSources` | boolean | no | Include source metadata when using structured output. Default: `false`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native LinkupAPI API returns.

## Native endpoint

Through the native LinkupAPI API, this operation is `POST /search` (base URL `https://api.linkup.so/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search.md) for the provider-specific parameters and requirements.

