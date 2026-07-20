# Send SMS/MMS with JustCall

Creates an SMS or MMS message in JustCall.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2.1/texts/new`
- **Base URL:** `https://api.justcall.io`
- **Official documentation:** [Send SMS/MMS](https://developer.justcall.io/reference/texts_new_v21)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `justcall_number` | body | `string` | yes |
| `body` | body | `string` | yes |
| `contact_number` | body | `string` | yes |
| `media_url` | body | `string` | no |
| `restrict_once` | body | `string` | no |
| `schedule_at` | body | `string` | no |
