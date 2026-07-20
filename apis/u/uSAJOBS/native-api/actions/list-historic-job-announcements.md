# List Historic Job Announcements with USAJOBS

Retrieves historic job announcements from USAJOBS.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/historicjoa`
- **Base URL:** `https://data.usajobs.gov`
- **Official documentation:** [List Historic Job Announcements](https://developer.usajobs.gov/api-reference/get-api-historicjoa)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `HiringAgencyCodes` | query | `string` | no | Agency code in which the position is located. |
