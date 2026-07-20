# Metronome: Get Billable Metric

Retrieves a billable metric from Metronome.

```
GET https://connect.mindcloud.co/v1/universal/metronome/latest/actions/get-billable-metric
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Metronome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/metronome/latest/actions/get-billable-metric?connectionId=$CONNECTION_ID&billableMetricId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "billableMetricId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/metronome/latest/actions/get-billable-metric?${params}`, {
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
| `billableMetricId` | string | yes | The billable metric ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aggregation_key": "string",
      "aggregation_type": "string",
      "event_type_filter": {
        "in_values": [
          "string"
        ]
      },
      "group_keys[]": [
        "string"
      ],
      "id": "string",
      "name": "Ava Chen",
      "property_filters": [
        {
          "exists": true,
          "name": "Ava Chen"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aggregation_key` | string |  |
| `aggregation_type` | string |  |
| `event_type_filter.in_values[]` | string |  |
| `group_keys[][]` | string |  |
| `id` | string |  |
| `name` | string |  |
| `property_filters[].exists` | boolean |  |
| `property_filters[].name` | string |  |

## Native endpoint

Through the native Metronome API, this operation is `GET /v1/billable-metrics/:billable_metric_id` (base URL `https://api.metronome.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-billable-metric.md) for the provider-specific parameters and requirements.

