# Count Active Alerts with Umbrella

Retrieves the count of active alerts from Umbrella.

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.sse.cisco.com/admin/v2/alerting/alerts?filters={"only_active_alerts_count":true}`
- **Base URL:** `https://api.umbrella.com`
- **Official documentation:** [Count Active Alerts](https://developer.cisco.com/docs/cloud-security/list-alerts/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
