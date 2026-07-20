# Customer.io: Get Transactional Message Metrics

Retrieves metrics for a Customer.io transactional message.

```
GET https://connect.mindcloud.co/v1/universal/customerio/latest/actions/get-transactional-message-metrics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Customer.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/customerio/latest/actions/get-transactional-message-metrics?connectionId=$CONNECTION_ID&transactionalId=3" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "transactionalId": "3"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/customerio/latest/actions/get-transactional-message-metrics?${params}`, {
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
| `transactionalId` | number | yes | The identifier of your transactional message. Example: `3`. |
| `period` | list<string> | no | The unit of time for your report. One of: `days`, `hours`, `months`, `weeks`. Example: `days`. |
| `steps` | number | no | The number of periods you want to return. Example: `7`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "end": "2026-05-07T12:00:00.000Z",
      "metric": {},
      "res": "string",
      "start": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `end` | date | The end of the metrics range. |
| `metric` | object | Metric series arrays keyed by metric name. |
| `res` | string | The reporting resolution returned by Customer.io. |
| `start` | date | The beginning of the metrics range. |

## Native endpoint

Through the native Customer.io API, this operation is `GET /v1/transactional/:transactional_id/metrics` (base URL `https://api.customer.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transactional-message-metrics.md) for the provider-specific parameters and requirements.

