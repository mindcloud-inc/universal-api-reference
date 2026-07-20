# Get Company Owners with OpenRegister

Retrieves a company's owners from OpenRegister.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/company/:company_id/owners`
- **Base URL:** `https://api.openregister.de`
- **Official documentation:** [Get Company Owners](https://docs.openregister.de/endpoint/company-owners)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | path | `string` | yes | Unique company identifier. |
