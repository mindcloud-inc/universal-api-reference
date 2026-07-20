# Customer.io: Get Newsletter Metrics

Retrieves metrics for a Customer.io newsletter.

```
GET https://connect.mindcloud.co/v1/universal/customerio/latest/actions/get-newsletter-metrics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Customer.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/customerio/latest/actions/get-newsletter-metrics?connectionId=$CONNECTION_ID&newsletterId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "newsletterId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/customerio/latest/actions/get-newsletter-metrics?${params}`, {
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
| `newsletterId` | number | yes | The numeric ID of the newsletter whose metrics you want to retrieve. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `period` | list<string> | no | Unit of time for the returned report. One of: `days`, `hours`, `months`, `weeks`. Default: `days`. |
| `steps` | number | no | Number of periods to include in the report. |
| `type` | list<string> | no | Limit metrics to one message type such as email, push, or in_app. One of: `email`, `in_app`, `push`, `slack`, `twilio`, `webhook`, `whatsapp`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "metric": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `metric` | object | Metric series arrays keyed by metric name. |

## Native endpoint

Through the native Customer.io API, this operation is `GET /v1/newsletters/:newsletter_id/metrics` (base URL `https://api.customer.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-newsletter-metrics.md) for the provider-specific parameters and requirements.

