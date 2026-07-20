# Get Company UBOs with OpenRegister

Retrieves a company's ultimate beneficial owners from OpenRegister.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/company/:company_id/ubo`
- **Base URL:** `https://api.openregister.de`
- **Official documentation:** [Get Company UBOs](https://docs.openregister.de/endpoint/company-ubo)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | path | `string` | yes | Unique company identifier. |
