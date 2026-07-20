# Get Audit Event Info with Dotcom Monitor

Retrieves audit event details from Dotcom Monitor.

## Endpoint

- **Method:** `GET`
- **Path:** `/audit/object/:sample_id`
- **Base URL:** `https://api.dotcom-monitor.com/config_api_v1`
- **Official documentation:** [Get Audit Event Info](https://www.dotcom-monitor.com/wiki/knowledge-base/get-audit-event-info/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sample_id` | path | `string` | yes | Unique audit event id from Get Audit Object List. |
