# Get Newsletter Metrics with Customer.io

Retrieves metrics for a Customer.io newsletter.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/newsletters/:newsletter_id/metrics`
- **Base URL:** `https://api.customer.io`
- **Official documentation:** [Get Newsletter Metrics](https://docs.customer.io/integrations/api/app/#tag/Newsletters/operation/getNewsletterMetrics)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `newsletter_id` | path | `number` | yes | The numeric ID of the newsletter whose metrics you want to retrieve. |
| `period` | query | `list<string>` | no | Unit of time for the returned report. Accepted values: `days`, `hours`, `months`, `weeks`. |
| `steps` | query | `number` | no | Number of periods to include in the report. |
| `type` | query | `list<string>` | no | Limit metrics to one message type such as email, push, or in_app. Accepted values: `email`, `in_app`, `push`, `slack`, `twilio`, `webhook`, `whatsapp`. |
