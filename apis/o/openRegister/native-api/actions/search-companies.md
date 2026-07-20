# Search Companies with OpenRegister

Finds companies in OpenRegister by name or register details.

## Endpoint

- **Method:** `GET`
- **Path:** `/v0/search/company`
- **Base URL:** `https://api.openregister.de`
- **Official documentation:** [Search Companies](https://docs.openregister.de/endpoint/search-company)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | no | Text search query to find companies by name. |
| `register_number` | query | `string` | no | Company register number for exact matching. |
| `register_type` | query | `string` | no | Type of company register, such as HRB, HRA, PR, GnR, or VR. |
| `register_court` | query | `string` | no | Court where the company is registered. |
| `active` | query | `boolean` | no | Filter for active or inactive companies. |
| `legal_form` | query | `string` | no | Legal form of the company, such as gmbh, ag, ug, kg, or ohg. |
| `incorporation_date` | query | `date` | no | Date of incorporation in YYYY-MM-DD format. |
