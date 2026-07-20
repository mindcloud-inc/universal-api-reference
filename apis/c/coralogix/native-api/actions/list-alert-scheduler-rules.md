# List Alert Scheduler Rules with Coralogix

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/alert-scheduler-rules/bulk`
- **Base URL:** `https://api.eu2.coralogix.com/mgmt/openapi/latest`
- **Official documentation:** [List Alert Scheduler Rules](https://docs.coralogix.com/api-reference/latest/alert-scheduler-rule-service/get-bulk-alert-scheduler-rule)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `active_timeframe` | query | `string` | no | Optional active_timeframe query parameter supported by the Coralogix OpenAPI endpoint. |
| `enabled` | query | `boolean` | no | Optional enabled query parameter supported by the Coralogix OpenAPI endpoint. |
| `alert_scheduler_rules_ids` | query | `string` | no | Optional alert_scheduler_rules_ids query parameter supported by the Coralogix OpenAPI endpoint. |
| `next_page_token` | query | `string` | no | Optional next_page_token query parameter supported by the Coralogix OpenAPI endpoint. |
