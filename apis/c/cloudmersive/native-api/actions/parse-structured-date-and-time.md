# Parse Structured Date and Time with Cloudmersive

Parses a structured date and time in Cloudmersive.

## Endpoint

- **Method:** `POST`
- **Path:** `/validate/date-time/parse/date-time/structured`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Parse Structured Date and Time](https://api.cloudmersive.com/docs/validate.asp#operation--validate-date-time-parse-date-time-structured-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CountryCode` | body | `string` | no | Optional country code used to optimize date parsing. |
| `RawDateTimeInput` | body | `string` | no | Standardized date-time string to parse. |
