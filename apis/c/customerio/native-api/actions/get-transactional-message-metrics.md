# Get Transactional Message Metrics with Customer.io

Retrieves metrics for a Customer.io transactional message.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/transactional/:transactional_id/metrics`
- **Base URL:** `https://api.customer.io`
- **Official documentation:** [Get Transactional Message Metrics](https://docs.customer.io/integrations/api/app/#tag/Transactional/operation/transactionalMetrics)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transactional_id` | path | `number` | yes | The identifier of your transactional message. |
| `period` | query | `list<string>` | no | The unit of time for your report. Accepted values: `days`, `hours`, `months`, `weeks`. |
| `steps` | query | `number` | no | The number of periods you want to return. |
