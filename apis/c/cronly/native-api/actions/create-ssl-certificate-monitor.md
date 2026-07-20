# Create SSL Certificate Monitor with Cronly

## Endpoint

- **Method:** `POST`
- **Path:** `/api/certificates`
- **Base URL:** `https://cronly.app`
- **Official documentation:** [Create SSL Certificate Monitor](https://docs.cronly.app/api/cron-job-monitor-4)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hostname` | body | `string` | yes | Hostname of the SSL certificate monitor. |
| `port` | body | `number` | no | Port to check. Defaults to 443. |
| `project_id` | body | `number` | no | Optional project to associate with the certificate monitor. |
