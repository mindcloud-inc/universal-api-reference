# List Template Fields with NileDesk

Retrieves fields for a NileDesk template.

## Endpoint

- **Method:** `POST`
- **Path:** `/GetFields`
- **Base URL:** `https://app.niledesk.com/api/public`
- **Official documentation:** [List Template Fields](https://niledesk.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template_id` | body | `string` | no | The NileDesk template identifier whose fields should be returned. |
