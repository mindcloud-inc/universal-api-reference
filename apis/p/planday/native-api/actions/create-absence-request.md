# Create Absence Request with Planday

Creates a new absence request in Planday.

## Endpoint

- **Method:** `POST`
- **Path:** `/absence/v1.0/absencerequests`
- **Base URL:** `https://openapi.planday.com`
- **Official documentation:** [Create Absence Request](https://openapi.planday.com/api/absence/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `absencePeriod` | body | `object` | yes |
| `absenceType` | body | `string` | no |
| `note` | body | `string` | no |
| `registrations[]` | body | `array<object>` | yes |
