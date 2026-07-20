# Find Company with Captain Data

Finds a company in Captain Data by company name.

## Endpoint

- **Method:** `GET`
- **Path:** `/companies/find`
- **Base URL:** `https://api.captaindata.com/v1`
- **Official documentation:** [Find Company](https://docs.captaindata.com/v1/api/companies/find)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_name` | query | `string` | yes | Company name to resolve to a Captain Data company UID. |
