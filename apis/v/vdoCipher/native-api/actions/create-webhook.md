# Create Webhook with VdoCipher

Creates a new webhook in VdoCipher.

## Endpoint

- **Method:** `POST`
- **Path:** `/hooks/`
- **Base URL:** `https://dev.vdocipher.com/api`
- **Official documentation:** [Create Webhook](https://www.vdocipher.com/docs/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `event` | body | `string` | no |
| `status` | body | `string` | no |
| `type` | body | `string` | no |
| `value` | body | `string` | no |
