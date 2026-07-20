# Submit Opt-In with Flexmail

Creates an opt-in form submission in Flexmail.

## Endpoint

- **Method:** `POST`
- **Path:** `/opt-ins`
- **Base URL:** `https://api.flexmail.eu`
- **Official documentation:** [Submit Opt-In](https://api.flexmail.eu/documentation/#post-/opt-ins)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `email` | body | `string` | yes |
| `opt_in_form_id` | body | `number` | yes |
| `first_name` | body | `string` | no |
| `name` | body | `string` | no |
| `language` | body | `string` | no |
| `custom_fields` | body | `object` | no |
