# List Corrections with eCFR

Retrieves a list of corrections from eCFR.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/admin/v1/corrections.json`
- **Base URL:** `https://www.ecfr.gov`
- **Official documentation:** [List Corrections](https://www.ecfr.gov/developers/documentation/api/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | query | `number` | no | Optional CFR title number to filter corrections, such as 1. |
