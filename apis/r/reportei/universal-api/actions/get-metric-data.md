# Reportei: Get Metric Data

Retrieves metric data from Reportei.

```
GET https://connect.mindcloud.co/v1/universal/reportei/latest/actions/get-metric-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reportei `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reportei/latest/actions/get-metric-data?connectionId=$CONNECTION_ID&start=2026-05-07T12%3A00%3A00.000Z&end=2026-05-07T12%3A00%3A00.000Z&integrationId=1&metrics%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "start": "2026-05-07T12:00:00.000Z",
  "end": "2026-05-07T12:00:00.000Z",
  "integrationId": "1",
  "metrics[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reportei/latest/actions/get-metric-data?${params}`, {
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
| `start` | date | yes | Data de início do período. |
| `end` | date | yes | Data de fim do período. |
| `integrationId` | number | yes | ID da integração. |
| `metrics[]` | array<object> | yes | Array de métricas a serem consultadas. |
| `comparisonStart` | date | no | Data de início do período de comparação. |
| `comparisonEnd` | date | no | Data de fim do período de comparação. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Metric values keyed by metric identifier |

## Native endpoint

Through the native Reportei API, this operation is `POST /metrics/get-data` (base URL `https://app.reportei.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-metric-data.md) for the provider-specific parameters and requirements.

