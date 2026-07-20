# Find People with Captain Data

Finds a person in Captain Data by full name.

## Endpoint

- **Method:** `GET`
- **Path:** `/people/find`
- **Base URL:** `https://api.captaindata.com/v1`
- **Official documentation:** [Find People](https://docs.captaindata.com/v1/api/people/find)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `full_name` | query | `string` | yes | Exact full name to look up. |
| `company_name` | query | `string` | no | Optional company name to disambiguate the person search. |
