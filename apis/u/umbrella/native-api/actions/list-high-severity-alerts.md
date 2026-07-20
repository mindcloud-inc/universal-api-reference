# List High Severity Alerts with Umbrella

Retrieves high-severity alert records from Umbrella.

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.sse.cisco.com/admin/v2/alerting/alerts?filters={"severity":1}`
- **Base URL:** `https://api.umbrella.com`
- **Official documentation:** [List High Severity Alerts](https://developer.cisco.com/docs/cloud-security/list-alerts/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
