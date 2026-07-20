# Get Full Title XML with eCFR

Retrieves the full XML for a title from eCFR.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/versioner/v1/full/:date/title-:title.xml`
- **Base URL:** `https://www.ecfr.gov`
- **Official documentation:** [Get Full Title XML](https://www.ecfr.gov/developers/documentation/api/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | path | `string` | yes | eCFR version date in YYYY-MM-DD format. |
| `title` | path | `number` | yes | CFR title number, such as 1. |
| `part` | query | `string` | no | Optional CFR part identifier to limit returned XML, such as 1. |
| `section` | query | `string` | no | Optional section identifier, such as 1.1. |
