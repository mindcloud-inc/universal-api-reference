# Get Broadcast Metrics with Customer.io

Retrieves metrics for a Customer.io broadcast.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/broadcasts/:broadcast_id/metrics`
- **Base URL:** `https://api.customer.io`
- **Official documentation:** [Get Broadcast Metrics](https://docs.customer.io/integrations/api/app/#tag/Broadcasts/operation/broadcastMetrics)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `broadcast_id` | path | `number` | yes | The numeric ID of the broadcast whose metrics you want to retrieve. |
| `period` | query | `list<string>` | no | Unit of time for the returned report. Accepted values: `days`, `hours`, `months`, `weeks`. |
| `steps` | query | `number` | no | Number of periods to include in the report. |
| `type` | query | `list<string>` | no | Limit metrics to one message type such as email, push, or in_app. Accepted values: `email`, `in_app`, `push`, `slack`, `twilio`, `webhook`, `whatsapp`. |
