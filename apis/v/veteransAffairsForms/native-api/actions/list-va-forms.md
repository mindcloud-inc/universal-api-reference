# List VA Forms with Veterans Affairs Forms

Finds VA forms by number, keyword, or title.

## Endpoint

- **Method:** `GET`
- **Path:** `/forms`
- **Base URL:** `https://sandbox-api.va.gov/services/va_forms/v0`
- **Official documentation:** [List VA Forms](https://developer.va.gov/explore/api/va-forms/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | no | Optional form number, keyword, or title used to filter VA forms. |
