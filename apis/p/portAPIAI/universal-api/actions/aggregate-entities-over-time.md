# Port API AI: Aggregate Entities Over Time

Retrieves entity aggregates over time from Port.

```
GET https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/aggregate-entities-over-time
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Port API AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/aggregate-entities-over-time?connectionId=$CONNECTION_ID&aggregationType=string&blueprint=string&func=string&properties%5B%5D=string&measureTimeBy=string&query=%5Bobject%20Object%5D&timeInterval=string&timeRange=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "aggregationType": "string",
  "blueprint": "string",
  "func": "string",
  "properties[]": "string",
  "measureTimeBy": "string",
  "query": "[object Object]",
  "timeInterval": "string",
  "timeRange": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/aggregate-entities-over-time?${params}`, {
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
| `aggregationType` | string | yes | Aggregation mode discriminator for Port aggregate-over-time |
| `blueprint` | string | yes | Blueprint identifier |
| `func` | string | yes | Aggregation function |
| `properties[]` | array<string> | yes | Property paths to aggregate |
| `measureTimeBy` | string | yes | Time property path used for bucketing |
| `query` | object | yes | Port search query object |
| `timeInterval` | string | yes | Bucket interval |
| `timeRange` | object | yes | Preset time range object |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ok": true,
      "result": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ok` | boolean |  |
| `result` | object |  |

## Native endpoint

Through the native Port API AI API, this operation is `POST /entities/aggregate-over-time` (base URL `https://api.port.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/aggregate-entities-over-time.md) for the provider-specific parameters and requirements.

