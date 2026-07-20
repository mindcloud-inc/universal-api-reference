# Get Committee with OpenFEC

Retrieves a committee from OpenFEC.

## Endpoint

- **Method:** `GET`
- **Path:** `/committee/:committee_id/`
- **Base URL:** `https://api.open.fec.gov/v1`
- **Official documentation:** [Get Committee](https://api.open.fec.gov/developers/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `committee_id` | path | `string` | yes | FEC committee ID, such as C00580100. |
