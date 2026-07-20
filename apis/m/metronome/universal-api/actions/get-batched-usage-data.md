# Metronome: Get Batched Usage Data

Retrieves batched usage data from Metronome.

```
GET https://connect.mindcloud.co/v1/universal/metronome/latest/actions/get-batched-usage-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Metronome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/metronome/latest/actions/get-batched-usage-data?connectionId=$CONNECTION_ID&windowSize=string&startingOn=string&endingBefore=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "windowSize": "string",
  "startingOn": "string",
  "endingBefore": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/metronome/latest/actions/get-batched-usage-data?${params}`, {
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
| `windowSize` | string | yes | Aggregation window size. |
| `startingOn` | string | yes | Start of the usage window. |
| `endingBefore` | string | yes | End of the usage window. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billable_metric_id": "string",
      "billable_metric_name": "Ava Chen",
      "customer_id": "string",
      "end_timestamp": "2026-05-07T12:00:00.000Z",
      "start_timestamp": "2026-05-07T12:00:00.000Z",
      "value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billable_metric_id` | string |  |
| `billable_metric_name` | string |  |
| `customer_id` | string |  |
| `end_timestamp` | date |  |
| `start_timestamp` | date |  |
| `value` | number |  |

## Native endpoint

Through the native Metronome API, this operation is `POST /v1/usage` (base URL `https://api.metronome.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-batched-usage-data.md) for the provider-specific parameters and requirements.

