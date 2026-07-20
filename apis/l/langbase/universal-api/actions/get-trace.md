# Langbase: Get Trace



```
GET https://connect.mindcloud.co/v1/universal/langbase/latest/actions/get-trace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Langbase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/langbase/latest/actions/get-trace?connectionId=$CONNECTION_ID&traceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "traceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/langbase/latest/actions/get-trace?${params}`, {
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
| `traceId` | string | yes | Trace ID to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "documentName": "Ava Chen",
      "documentSize": 1,
      "documentType": "string",
      "duration": 1,
      "id": "string",
      "orgId": "string",
      "output": [
        "string"
      ],
      "parameters": {},
      "tokens": {},
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `documentName` | string |  |
| `documentSize` | number |  |
| `documentType` | string |  |
| `duration` | number |  |
| `id` | string |  |
| `orgId` | string |  |
| `output` | array<string> |  |
| `parameters` | object |  |
| `tokens` | object |  |
| `userId` | string |  |

## Native endpoint

Through the native Langbase API, this operation is `GET v1/traces/:traceId` (base URL `https://api.langbase.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-trace.md) for the provider-specific parameters and requirements.

