# Webcrawler API: Resend Crawl Job Webhook

Resends a crawl job webhook from Webcrawler API.

```
PUT https://connect.mindcloud.co/v1/universal/webcrawlerAPI/latest/actions/resend-crawl-job-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webcrawler API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/webcrawlerAPI/latest/actions/resend-crawl-job-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webcrawlerAPI/latest/actions/resend-crawl-job-webhook', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Completed crawl job identifier returned by Create Crawl Job or Get Crawl Job. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "job_id": "string",
      "message": "string",
      "status_code": 1,
      "success": true,
      "webhook_error": "string",
      "webhook_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `job_id` | string | Crawl job identifier that the webhook was resent for. |
| `message` | string | Provider resend status message. |
| `status_code` | number | HTTP status code returned by the webhook receiver. |
| `success` | boolean | Whether the webhook resend succeeded. |
| `webhook_error` | string | Webhook delivery error returned by the provider when present. |
| `webhook_url` | string | Webhook URL that received the resend attempt. |

## Native endpoint

Through the native Webcrawler API API, this operation is `POST /v1/job/:id/webhook/resend` (base URL `https://api.webcrawlerapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/resend-crawl-job-webhook.md) for the provider-specific parameters and requirements.

