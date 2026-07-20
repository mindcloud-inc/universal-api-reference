# Create Monitor with Postman

Creates a new monitor in Postman.

## Endpoint

- **Method:** `POST`
- **Path:** `/monitors`
- **Base URL:** `https://api.getpostman.com`
- **Official documentation:** [Create Monitor](https://www.postman.com/postman/postman-public-workspace/request/xae4ivm/create-a-monitor)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace` | query | `string` | no |
| `monitor.name` | body | `string` | yes |
| `monitor.collection` | body | `string` | yes |
| `monitor.environment` | body | `string` | no |
| `monitor.schedule.cron` | body | `string` | yes |
| `monitor.schedule.timezone` | body | `string` | yes |
