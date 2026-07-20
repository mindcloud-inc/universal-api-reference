# Get Company Holdings with OpenRegister

Retrieves a company's holdings from OpenRegister.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/company/:company_id/holdings`
- **Base URL:** `https://api.openregister.de`
- **Official documentation:** [Get Company Holdings](https://docs.openregister.de/endpoint/company-holdings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | path | `string` | yes | Unique company identifier. |
