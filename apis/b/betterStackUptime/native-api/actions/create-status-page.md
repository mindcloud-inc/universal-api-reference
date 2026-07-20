# Create Status Page with Better Stack Uptime

Creates a new status page in Better Stack Uptime.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/status-pages`
- **Base URL:** `https://uptime.betterstack.com/api`
- **Official documentation:** [Create Status Page](https://betterstack.com/docs/uptime/api/create-a-new-status-page/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_name` | body | `string` | yes | Status page company name. |
| `company_url` | body | `string` | yes | Public company URL shown on the status page. |
| `subdomain` | body | `string` | yes | Unique Better Stack status page subdomain. |
| `timezone` | body | `string` | yes | Status page timezone, for example UTC. |
| `automatic_reports` | body | `boolean` | no | Enable automatic reports for the page. |
| `subscribable` | body | `boolean` | no | Allow subscribers to opt into page updates. |
