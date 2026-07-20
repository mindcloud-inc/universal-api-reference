# Statsig: Retrieve Pulse Metric Result

Retrieves a pulse metric result from Statsig.

```
GET https://connect.mindcloud.co/v1/universal/statsig/latest/actions/retrieve-pulse-metric-result-get-console-v1-experiments-id-pulse-metric-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statsig `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/statsig/latest/actions/retrieve-pulse-metric-result-get-console-v1-experiments-id-pulse-metric-result?connectionId=$CONNECTION_ID&id=string&control=string&test=string&metricID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "control": "string",
  "test": "string",
  "metricID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/statsig/latest/actions/retrieve-pulse-metric-result-get-console-v1-experiments-id-pulse-metric-result?${params}`, {
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
| `id` | string | yes | id |
| `control` | string | yes | Control Group ID |
| `test` | string | yes | Test Group ID |
| `metricID` | string | yes | Metric ID in format <metric_name>::<metric_type> |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cuped` | string | no | Whether to apply CUPED. Allowed values are "true" or "false". |
| `confidence` | string | no | Confidence interval (0-100) |
| `applyBonferroniPerVariant` | string | no | Whether to apply Bonferroni Per Variant. Allowed values are "true" or "false". |
| `applyBonferroniPerMetric` | string | no | Whether to apply Bonferroni Per Metric. Allowed values are "true" or "false". |
| `bonferroniPrimaryMetricWeight` | string | no | α allocated to primary metrics |
| `applyBenjaminiHochbergPerMetric` | string | no | Whether to apply Benjamini-Hochberg Correction Per Metric. Allowed values are "true" or "false". |
| `applyBenjaminiHochbergPerVariant` | string | no | Whether to apply Benjamini-Hochberg Correction Per Variant. Allowed values are "true" or "false". |
| `date` | string | no | Date for pulse results. format must be YYYY-MM-DD |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Statsig response data payload. |
| `message` | string | Statsig response message. |

## Native endpoint

Through the native Statsig API, this operation is `GET /console/v1/experiments/{id}/pulse_metric_result` (base URL `https://statsigapi.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-pulse-metric-result-get-console-v1-experiments-id-pulse-metric-result.md) for the provider-specific parameters and requirements.

