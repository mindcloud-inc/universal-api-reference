# Get VA Form with Veterans Affairs Forms

Retrieves a VA form by form name.

## Endpoint

- **Method:** `GET`
- **Path:** `/forms/:form_name`
- **Base URL:** `https://sandbox-api.va.gov/services/va_forms/v0`
- **Official documentation:** [Get VA Form](https://developer.va.gov/explore/api/va-forms/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_name` | path | `string` | yes | Exact VA form name, including proper placement of prefixes and hyphens. Example: 10-10EZ. |
