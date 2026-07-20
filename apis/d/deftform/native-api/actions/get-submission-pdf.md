# Get Submission PDF with Deftform

Retrieves a submission PDF link from Deftform.

## Endpoint

- **Method:** `GET`
- **Path:** `/response/:uuid/pdf`
- **Base URL:** `https://deftform.com/api/v1`
- **Official documentation:** [Get Submission PDF](https://help.deftform.com/api/endpoints)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuid` | path | `string` | yes | The submission UUID returned by the List Form Responses action. |
