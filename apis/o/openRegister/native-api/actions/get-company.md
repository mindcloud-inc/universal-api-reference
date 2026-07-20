# Get Company with OpenRegister

Retrieves company information from OpenRegister by company ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/company/:company_id`
- **Base URL:** `https://api.openregister.de`
- **Official documentation:** [Get Company](https://docs.openregister.de/endpoint/company)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | path | `string` | yes | Unique company identifier. |
| `realtime` | query | `boolean` | no | Fetch latest Handelsregister data when true. Increases credit cost. |
