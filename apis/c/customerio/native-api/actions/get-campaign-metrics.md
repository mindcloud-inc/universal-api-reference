# Get Campaign Metrics with Customer.io

Retrieves metrics for a Customer.io campaign.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/campaigns/:campaign_id/metrics`
- **Base URL:** `https://api.customer.io`
- **Official documentation:** [Get Campaign Metrics](https://docs.customer.io/integrations/api/app/#tag/Campaigns/operation/campaignMetrics)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | path | `number` | yes | The numeric ID of the campaign whose metrics you want to retrieve. |
| `version` | query | `list<string>` | yes | The metrics API version. Customer.io recommends version 2 for this endpoint. Accepted values: `1`, `2`. |
| `type` | query | `list<string>` | no | Limit metrics to one message type such as email, push, or in_app. Accepted values: `email`, `in_app`, `push`, `slack`, `twilio`, `webhook`, `whatsapp`. |
| `res` | query | `list<string>` | no | Version 2 only. Bucket metrics hourly, daily, weekly, or monthly. Accepted values: `daily`, `days`, `hourly`, `hours`, `monthly`, `months`, `weekly`, `weeks`. |
| `tz` | query | `string` | no | Version 2 only. Region-style time zone such as America/New_York. |
| `start` | query | `number` | no | Version 2 only. Unix timestamp for the beginning of the metrics window. |
| `end` | query | `number` | no | Version 2 only. Unix timestamp for the end of the metrics window. |
| `period` | query | `list<string>` | no | Version 1 only. Unit of time for the returned report. Accepted values: `days`, `hours`, `months`, `weeks`. |
| `steps` | query | `number` | no | Version 1 only. Number of periods to include in the report. |
