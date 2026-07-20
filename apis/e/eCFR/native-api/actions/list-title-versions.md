# List Title Versions with eCFR

Retrieves the available versions for a title from eCFR.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/versioner/v1/versions/title-:title.json`
- **Base URL:** `https://www.ecfr.gov`
- **Official documentation:** [List Title Versions](https://www.ecfr.gov/developers/documentation/api/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | path | `number` | yes | CFR title number, such as 1. |
| `issue_date` | query | `string` | no | Optional issue date in YYYY-MM-DD format. |
| `part` | query | `string` | no | Optional CFR part identifier to filter versions. |
