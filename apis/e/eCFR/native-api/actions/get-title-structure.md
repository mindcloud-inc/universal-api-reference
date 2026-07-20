# Get Title Structure with eCFR

Retrieves a title structure from eCFR.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/versioner/v1/structure/:date/title-:title.json`
- **Base URL:** `https://www.ecfr.gov`
- **Official documentation:** [Get Title Structure](https://www.ecfr.gov/developers/documentation/api/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | path | `string` | yes | eCFR version date in YYYY-MM-DD format. |
| `title` | path | `number` | yes | CFR title number, such as 1. |
