# Create call with Vibrato

Creates a new call in Vibrato.

## Endpoint

- **Method:** `POST`
- **Path:** `/calls/`
- **Base URL:** `https://api.getvibrato.com/api/v1`
- **Official documentation:** [Create call](https://docs.getvibrato.com/api-reference/calls/create-a-new-call)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country_code` | body | `string` | yes | Phone country code, for example 1. |
| `phone_number` | body | `string` | yes | Phone number. |
| `prompt` | body | `string` | yes | Call prompt. |
| `locale` | body | `string` | no | Call locale. |
| `labels[]` | body | `array<string>` | no | Labels for the call. |
| `api_idempotency_key` | body | `string` | no | Optional idempotency key. |
| `tags[]` | body | `array<string>` | no | Tags. |
