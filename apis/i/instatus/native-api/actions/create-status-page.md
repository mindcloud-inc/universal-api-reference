# Create Status Page with Instatus

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/pages`
- **Base URL:** `https://api.instatus.com`
- **Official documentation:** [Create Status Page](https://instatus.com/help/api/status-pages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | Owner or contact email for the status page. |
| `name` | body | `string` | no | Status page name. |
| `subdomain` | body | `string` | no | Status page subdomain. |
