# Register Session Person with Livestorm

Registers a person for a session in Livestorm.

## Endpoint

- **Method:** `POST`
- **Path:** `sessions/:id/people`
- **Base URL:** `https://api.livestorm.co/v1`
- **Official documentation:** [Register Session Person](https://developers.livestorm.co/reference/post_sessions-id-people)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Session ID |
| `data.attributes.fields[]` | body | `array<object>` | no | — |
| `data.attributes.fields[].id` | body | `string` | no | — |
| `data.attributes.fields[].value` | body | `string` | no | — |
| `data.attributes.referrer` | body | `string` | no | — |
| `data.attributes.utm_source` | body | `string` | no | — |
| `data.attributes.utm_medium` | body | `string` | no | — |
| `data.attributes.utm_term` | body | `string` | no | — |
| `data.attributes.utm_content` | body | `string` | no | — |
| `data.attributes.utm_campaign` | body | `string` | no | — |
