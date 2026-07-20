# List User Task History with PiAPI/Flux.1

Retrieves user task history from PiAPI/Flux.1.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/open/tasks/histories`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [List User Task History](https://piapi.ai/docs/piapi-user-history-query)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `page` | query | `number` | no |
| `page_size` | query | `number` | no |
| `model` | query | `string` | no |
| `start_time` | query | `number` | no |
| `end_time` | query | `number` | no |
