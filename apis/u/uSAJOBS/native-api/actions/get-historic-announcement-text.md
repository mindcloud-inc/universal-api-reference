# Get Historic Announcement Text with USAJOBS

Retrieves historic announcement text from USAJOBS.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/historicjoa/announcementtext`
- **Base URL:** `https://data.usajobs.gov`
- **Official documentation:** [Get Historic Announcement Text](https://developer.usajobs.gov/api-reference/get-api-announcementtext)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `HiringAgencyCodes` | query | `string` | no | Agency code in which the position is located. |
