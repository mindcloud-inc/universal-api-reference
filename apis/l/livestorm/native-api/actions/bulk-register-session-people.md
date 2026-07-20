# Bulk Register Session People with Livestorm

Registers multiple people for a session in Livestorm.

## Endpoint

- **Method:** `POST`
- **Path:** `sessions/:id/people/bulk`
- **Base URL:** `https://api.livestorm.co/v1`
- **Official documentation:** [Bulk Register Session People](https://developers.livestorm.co/reference/post_sessions-id-people-bulk)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Session ID |
| `data.attributes.tasks[]` | body | `array<object>` | no | — |
| `data.attributes.tasks[].fields[]` | body | `array<object>` | no | — |
| `data.attributes.tasks[].fields[].id` | body | `string` | no | — |
| `data.attributes.tasks[].fields[].value` | body | `string` | no | — |
| `data.attributes.tasks[].referrer` | body | `string` | no | — |
| `data.attributes.tasks[].utm_source` | body | `string` | no | — |
| `data.attributes.tasks[].utm_medium` | body | `string` | no | — |
| `data.attributes.tasks[].utm_term` | body | `string` | no | — |
| `data.attributes.tasks[].utm_content` | body | `string` | no | — |
| `data.attributes.tasks[].utm_campaign` | body | `string` | no | — |
