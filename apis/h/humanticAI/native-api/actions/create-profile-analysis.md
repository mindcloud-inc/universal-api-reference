# Create Profile Analysis with Humantic AI

## Endpoint

- **Method:** `GET`
- **Path:** `/user-profile/create`
- **Base URL:** `https://api.humantic.ai/v1`
- **Official documentation:** [Create Profile Analysis](https://api.humantic.ai/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | yes | LinkedIn profile URL, email address, or another unique identifier for the individual being analyzed. Do not use values starting with `test`. |
| `firstname` | query | `string` | no | Optional first name. Helpful when the identifier is an email address. |
| `lastname` | query | `string` | no | Optional last name. Helpful when the identifier is an email address. |
| `enrichprofile` | query | `boolean` | no | For eligible plans and email identifiers, controls whether Humantic tries to resolve associated social profile data. |
