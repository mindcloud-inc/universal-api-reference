# Lookup Person And Company with RocketReach

Retrieves a person and company from RocketReach.

## Endpoint

- **Method:** `GET`
- **Path:** `/profile-company/lookup`
- **Base URL:** `https://api.rocketreach.co/api/v2`
- **Official documentation:** [Lookup Person And Company](https://docs.rocketreach.co/reference/create_person_and_company_lookup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `current_employer` | query | `string` | no | — |
| `email` | query | `string` | no | — |
| `id` | query | `number` | no | — |
| `linkedin_url` | query | `string` | no | — |
| `lookup_type` | query | `string` | no | Standard, premium, bulk, phone, or enrich lookup mode. |
| `name` | query | `string` | no | — |
| `npi_number` | query | `number` | no | — |
| `title` | query | `string` | no | — |
| `webhook_id` | query | `number` | no | — |
