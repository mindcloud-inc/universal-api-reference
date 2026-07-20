# Deputy: List Labor Model Rules

Retrieves labor model rules from Deputy.

```
GET https://connect.mindcloud.co/v1/universal/deputy/latest/actions/list-labor-model-rules
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deputy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deputy/latest/actions/list-labor-model-rules?connectionId=$CONNECTION_ID&locationId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "locationId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deputy/latest/actions/list-labor-model-rules?${params}`, {
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
| `locationId` | number | yes | Deputy location ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "area": 1,
      "buffers": {},
      "coverage": 1,
      "id": "string",
      "laborAmount": 1,
      "maxLabor": 1,
      "maxMetricAmount": 1,
      "metric": "string",
      "metricAmount": "string",
      "metricValueType": "string",
      "minLabor": 1,
      "steps": [
        {}
      ],
      "subMetric": "string",
      "timeframe": 1,
      "useBuffers": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `area` | number |  |
| `buffers` | object |  |
| `coverage` | number |  |
| `id` | string |  |
| `laborAmount` | number |  |
| `maxLabor` | number |  |
| `maxMetricAmount` | number |  |
| `metric` | string |  |
| `metricAmount` | string |  |
| `metricValueType` | string |  |
| `minLabor` | number |  |
| `steps` | array<object> |  |
| `subMetric` | string |  |
| `timeframe` | number |  |
| `useBuffers` | boolean |  |

## Native endpoint

Through the native Deputy API, this operation is `GET /api/v2/labor-model/location/:locationId/rules` (base URL `https://{{credentials.endpoint}}.deputy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-labor-model-rules.md) for the provider-specific parameters and requirements.

