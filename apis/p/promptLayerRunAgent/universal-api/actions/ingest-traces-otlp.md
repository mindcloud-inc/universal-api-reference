# PromptLayer Run Agent: Ingest Traces (OTLP)

Ingests trace data into PromptLayer using OTLP.

```
POST https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/ingest-traces-otlp
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PromptLayer Run Agent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/ingest-traces-otlp" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "resourceSpans[]": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/ingest-traces-otlp', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "resourceSpans[]": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `resourceSpans[]` | array<object> | yes | OTLP ExportTraceServiceRequest resourceSpans payload in JSON encoding. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "partialSuccess": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `partialSuccess` | object | OTLP partial success details. Null when all spans are accepted. |

## Native endpoint

Through the native PromptLayer Run Agent API, this operation is `POST /v1/traces` (base URL `https://api.promptlayer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/ingest-traces-otlp.md) for the provider-specific parameters and requirements.

