# Logit: Get Stack Diagnostics

Retrieves stack diagnostics from Logit.

```
GET https://connect.mindcloud.co/v1/universal/logit/latest/actions/get-stack-diagnostics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Logit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/logit/latest/actions/get-stack-diagnostics?connectionId=$CONNECTION_ID&stackId=string&page=1&pageSize=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "stackId": "string",
  "page": "1",
  "pageSize": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/logit/latest/actions/get-stack-diagnostics?${params}`, {
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
| `stackId` | string | yes |  |
| `component` | string | no |  |
| `level` | string | no |  |
| `searchTerm` | string | no |  |
| `timeRange` | string | no |  |
| `page` | number | yes |  |
| `pageSize` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "logEntries": [
        {}
      ],
      "resultsSkipped": true,
      "totalLogs": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `logEntries` | array<object> |  |
| `resultsSkipped` | boolean |  |
| `totalLogs` | number |  |

## Native endpoint

Through the native Logit API, this operation is `GET /api/stacks/:stackId/diagnostics` (base URL `https://dashboard.logit.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-stack-diagnostics.md) for the provider-specific parameters and requirements.

