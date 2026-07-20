# Get Company Historical Owners with OpenRegister

Retrieves a company's historical owners from OpenRegister.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/company/:company_id/owners/historical`
- **Base URL:** `https://api.openregister.de`
- **Official documentation:** [Get Company Historical Owners](https://docs.openregister.de/endpoint/company-historical-owners)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | path | `string` | yes | Unique company identifier. |
