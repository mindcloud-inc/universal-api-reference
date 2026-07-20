# Fetch Companies with Swarm

Retrieves companies from Swarm by company ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/companies/fetch`
- **Base URL:** `https://bee.theswarm.com`
- **Official documentation:** [Fetch Companies](https://docs.theswarm.com/docs/endpoints/fetch-company)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields[]` | body | `array<string>` | no | Optional response fields such as company_info or tags. Provide a JSON array when needed. Send multiple values as a array. |
| `ids[]` | body | `array<string>` | yes | One or more Swarm company IDs to fetch. Provide a JSON array of IDs or add values in the UI. Send multiple values as a array. |
