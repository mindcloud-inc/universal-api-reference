# Discover Companies with Hunter

## Endpoint

- **Method:** `POST`
- **Path:** `/discover`
- **Base URL:** `https://api.hunter.io/v2`
- **Official documentation:** [Discover Companies](https://hunter.io/api-documentation/v2#discover)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `query` | body | `string` | no |
| `organization` | body | `object` | no |
| `similar_to` | body | `string` | no |
| `headquarters_location` | body | `object` | no |
| `industry` | body | `object` | no |
| `headcount` | body | `string` | no |
| `company_type` | body | `object` | no |
| `year_founded` | body | `object` | no |
| `keywords` | body | `object` | no |
| `technology` | body | `object` | no |
| `funding` | body | `object` | no |
| `limit` | body | `number` | no |
| `offset` | body | `number` | no |
