# Send Transactional Email with Loops

Creates a transactional email send in Loops.

## Endpoint

- **Method:** `POST`
- **Path:** `/transactional`
- **Base URL:** `https://app.loops.so/api/v1`
- **Official documentation:** [Send Transactional Email](https://loops.so/docs/api-reference/send-transactional-email)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `email` | body | `string` | yes |
| `transactionalId` | body | `string` | yes |
| `addToAudience` | body | `boolean` | no |
| `dataVariables` | body | `object` | no |
| `attachments[]` | body | `array<object>` | no |
| `attachments[].filename` | body | `string` | no |
| `attachments[].contentType` | body | `string` | no |
| `attachments[].data` | body | `string` | no |
