# LinkupAPI: Create Research Task

Creates a new research task in LinkupAPI.

```
POST https://connect.mindcloud.co/v1/universal/linkupAPI/latest/actions/create-research-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LinkupAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/linkupAPI/latest/actions/create-research-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "q": "string",
  "outputType": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/linkupAPI/latest/actions/create-research-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "q": "string",
    "outputType": "0"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `q` | string | yes | The natural-language research question to run. |
| `outputType` | string | yes | The research response format to request. One of: `0`, `1`. |
| `maxResults` | number | no | Maximum number of results to use in the research task. |
| `includeImages` | boolean | no | Include image results in the research context. Default: `false`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fromDate` | date | no | Only consider results on or after this ISO date. |
| `toDate` | date | no | Only consider results on or before this ISO date. |
| `includeDomains[]` | array<string> | no | Restrict research sources to these domains. |
| `excludeDomains[]` | array<string> | no | Exclude these domains from research sources. |
| `includeInlineCitations` | boolean | no | Include inline citations when the output type is sourcedAnswer. Default: `false`. |
| `structuredOutputSchema` | string | no | A JSON schema string describing the structured output to return when output type is structured. |
| `includeSources` | boolean | no | Include source metadata when using structured output. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | The ID of the created research task. |

## Native endpoint

Through the native LinkupAPI API, this operation is `POST /research` (base URL `https://api.linkup.so/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-research-task.md) for the provider-specific parameters and requirements.

