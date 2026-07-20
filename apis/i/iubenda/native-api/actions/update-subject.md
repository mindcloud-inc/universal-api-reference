# Update Subject with iubenda

Updates a subject in iubenda.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/subjects/:id`
- **Base URL:** `https://consent.iubenda.com`
- **Official documentation:** [Update Subject](https://www.iubenda.com/en/help/6484-consent-solution-http-api-documentation/#subjects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique identifier of the subject to update |
| `email` | body | `string` | no | Updated subject email address. |
| `first_name` | body | `string` | no | Updated subject first name. |
| `last_name` | body | `string` | no | Updated subject last name. |
| `full_name` | body | `string` | no | Updated subject full name. |
| `verified` | body | `boolean` | no | Updated subject verified status. |
| `phones[]` | body | `array<object>` | no | Array of phone objects for the subject. |
| `phones[].number` | body | `string` | no | A phone number with country code prefix. |
| `phones[].label` | body | `string` | no | Label used to identify the phone number. |
