# Logit: Get Stack Ingestion Spans

Retrieves stack ingestion spans from Logit.

```
GET https://connect.mindcloud.co/v1/universal/logit/latest/actions/get-stack-ingestion-spans
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Logit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/logit/latest/actions/get-stack-ingestion-spans?connectionId=$CONNECTION_ID&stackId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "stackId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/logit/latest/actions/get-stack-ingestion-spans?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "avgSpanCount": "string",
      "maxSpanCount": "string",
      "points": [
        {}
      ],
      "receivingData": true,
      "todaysDataSent": "string",
      "todaysSpanCount": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avgSpanCount` | string |  |
| `maxSpanCount` | string |  |
| `points` | array<object> |  |
| `receivingData` | boolean |  |
| `todaysDataSent` | string |  |
| `todaysSpanCount` | string |  |

## Native endpoint

Through the native Logit API, this operation is `GET /api/stacks/:stackId/ingestion/spans` (base URL `https://dashboard.logit.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-stack-ingestion-spans.md) for the provider-specific parameters and requirements.

