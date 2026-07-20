# Create Subject with iubenda

Creates a subject in iubenda.

## Endpoint

- **Method:** `POST`
- **Path:** `/subjects`
- **Base URL:** `https://consent.iubenda.com`
- **Official documentation:** [Create Subject](https://www.iubenda.com/en/help/6484-consent-solution-http-api-documentation/#subjects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | Subject email address. |
| `first_name` | body | `string` | no | Subject first name. |
| `last_name` | body | `string` | no | Subject last name. |
| `full_name` | body | `string` | no | Subject full name. |
| `verified` | body | `boolean` | no | Whether the subject is verified. |
| `phones[]` | body | `array<object>` | no | Array of phone objects for the subject. |
| `phones[].number` | body | `string` | no | A phone number with country code prefix. |
| `phones[].label` | body | `string` | no | Label used to identify the phone number. |
| `id` | body | `string` | no | Subject ID. Auto-filled by iubenda when omitted. |
