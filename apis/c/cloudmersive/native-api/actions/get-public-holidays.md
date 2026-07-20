# Get Public Holidays with Cloudmersive

Retrieves public holidays by country and year in Cloudmersive.

## Endpoint

- **Method:** `POST`
- **Path:** `/validate/date-time/get/holidays`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Get Public Holidays](https://api.cloudmersive.com/docs/validate.asp#operation--validate-date-time-get-holidays-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `RawCountryInput` | body | `string` | no | Two-letter country code for the holiday lookup. |
| `Year` | body | `string` | no | Optional year for the holiday lookup. |
