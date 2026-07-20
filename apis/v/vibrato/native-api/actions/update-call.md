# Update call with Vibrato

Updates an existing call in Vibrato.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/calls/{id}/`
- **Base URL:** `https://api.getvibrato.com/api/v1`
- **Official documentation:** [Update call](https://docs.getvibrato.com/api-reference/calls/update-an-existing-call)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Identifier from Vibrato. |
| `country_code` | body | `string` | yes | Phone country code, for example 1. |
| `phone_number` | body | `string` | yes | Phone number. |
| `prompt` | body | `string` | yes | Call prompt. |
| `locale` | body | `string` | no | Call locale. |
| `labels[]` | body | `array<string>` | no | Labels for the call. |
| `api_idempotency_key` | body | `string` | no | Optional idempotency key. |
| `tags[]` | body | `array<string>` | no | Tags. |
