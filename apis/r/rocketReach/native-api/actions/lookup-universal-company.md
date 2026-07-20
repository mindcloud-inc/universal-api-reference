# Lookup Universal Company with RocketReach

Retrieves a company from RocketReach Universal lookup.

## Endpoint

- **Method:** `GET`
- **Path:** `/universal/company/lookup`
- **Base URL:** `https://api.rocketreach.co/api/v2`
- **Official documentation:** [Lookup Universal Company](https://docs.rocketreach.co/reference/create_universal_company_lookup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | query | `string` | no | Domain of the desired company to look up. Preferred identifier. |
| `id` | query | `number` | no | RocketReach internal unique company ID. |
| `linkedin_url` | query | `string` | no | LinkedIn URL of the desired company to look up. |
| `name` | query | `string` | no | Name of the desired company to look up. |
| `ticker` | query | `string` | no | Stock ticker of the desired company to look up. |
