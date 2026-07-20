# Customer.io: Get Campaign Metrics

Retrieves metrics for a Customer.io campaign.

```
GET https://connect.mindcloud.co/v1/universal/customerio/latest/actions/get-campaign-metrics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Customer.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/customerio/latest/actions/get-campaign-metrics?connectionId=$CONNECTION_ID&campaignId=1&version=2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "1",
  "version": "2"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/customerio/latest/actions/get-campaign-metrics?${params}`, {
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
| `campaignId` | number | yes | The numeric ID of the campaign whose metrics you want to retrieve. |
| `version` | list<string> | yes | The metrics API version. Customer.io recommends version 2 for this endpoint. One of: `1`, `2`. Default: `2`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | list<string> | no | Limit metrics to one message type such as email, push, or in_app. One of: `email`, `in_app`, `push`, `slack`, `twilio`, `webhook`, `whatsapp`. |
| `resolution` | list<string> | no | Version 2 only. Bucket metrics hourly, daily, weekly, or monthly. One of: `daily`, `days`, `hourly`, `hours`, `monthly`, `months`, `weekly`, `weeks`. |
| `timezone` | string | no | Version 2 only. Region-style time zone such as America/New_York. |
| `start` | number | no | Version 2 only. Unix timestamp for the beginning of the metrics window. |
| `end` | number | no | Version 2 only. Unix timestamp for the end of the metrics window. |
| `period` | list<string> | no | Version 1 only. Unit of time for the returned report. One of: `days`, `hours`, `months`, `weeks`. |
| `steps` | number | no | Version 1 only. Number of periods to include in the report. |

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

Through the native Customer.io API, this operation is `GET /v1/campaigns/:campaign_id/metrics` (base URL `https://api.customer.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign-metrics.md) for the provider-specific parameters and requirements.

