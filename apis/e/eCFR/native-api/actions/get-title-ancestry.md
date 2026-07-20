# Get Title Ancestry with eCFR

Retrieves the ancestry for a title from eCFR.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/versioner/v1/ancestry/:date/title-:title.json`
- **Base URL:** `https://www.ecfr.gov`
- **Official documentation:** [Get Title Ancestry](https://www.ecfr.gov/developers/documentation/api/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | path | `string` | yes | eCFR version date in YYYY-MM-DD format. |
| `title` | path | `number` | yes | CFR title number, such as 1. |
| `section` | query | `string` | no | Optional section identifier, such as 1.1. |
| `part` | query | `string` | no | Optional CFR part identifier, such as 1. |
