# List Low Severity Alerts with Umbrella

Retrieves low-severity alert records from Umbrella.

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.sse.cisco.com/admin/v2/alerting/alerts?filters={"severity":3}`
- **Base URL:** `https://api.umbrella.com`
- **Official documentation:** [List Low Severity Alerts](https://developer.cisco.com/docs/cloud-security/list-alerts/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
