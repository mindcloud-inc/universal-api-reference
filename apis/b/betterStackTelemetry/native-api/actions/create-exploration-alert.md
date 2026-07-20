# Create Exploration Alert with Better Stack Telemetry

Creates a new exploration alert in Better Stack Telemetry.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/explorations/:exploration_id/alerts`
- **Base URL:** `https://telemetry.betterstack.com`
- **Official documentation:** [Create Exploration Alert](https://betterstack.com/docs/logs/api/alerts/create/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `exploration_id` | path | `string` | yes | The ID of the exploration to add the alert to. |
| `name` | body | `string` | yes | The name of the alert. |
| `alert_type` | body | `string` | yes | The type of alert. |
| `operator` | body | `string` | no | Comparison operator for threshold and relative alerts. |
| `value` | body | `number` | no | Numeric value for the alert condition. |
| `string_value` | body | `string` | no | Exact string match value for threshold alerts. |
| `anomaly_sensitivity` | body | `number` | no | Sensitivity for anomaly alerts. |
| `anomaly_trigger` | body | `string` | no | Which anomalies trigger the alert. |
| `query_period` | body | `number` | no | Time window in seconds for analyzed data. |
| `confirmation_period` | body | `number` | yes | Seconds the condition must hold before alerting. |
| `recovery_period` | body | `number` | no | Seconds the condition must be resolved before recovery. |
| `check_period` | body | `number` | no | How often to evaluate threshold and relative alerts. |
| `aggregation_interval` | body | `number` | no | Aggregation interval in seconds. |
| `series_names[]` | body | `array` | no | Series names to scope the alert to. |
| `source_variable` | body | `string` | no | Source variable used for source selection. |
| `source_mode` | body | `string` | no | Mode for source selection. |
| `source_platforms[]` | body | `array` | no | Platforms used for source selection. |
| `incident_cause` | body | `string` | no | Cause text included in incidents. |
| `incident_per_series` | body | `boolean` | no | Create a separate incident for each triggering series. |
| `escalation_target` | body | `object` | no | Notification target object. |
| `call` | body | `boolean` | no | Enable phone call notifications. |
| `sms` | body | `boolean` | no | Enable SMS notifications. |
| `email` | body | `boolean` | no | Enable email notifications. |
| `push` | body | `boolean` | no | Enable push notifications. |
| `critical_alert` | body | `boolean` | no | Enable critical push notifications. |
| `metadata` | body | `object` | no | Custom metadata object. |
| `paused` | body | `boolean` | no | Create the alert in a paused state. |
| `team_name` | body | `string` | no | Team name for global API tokens. |
