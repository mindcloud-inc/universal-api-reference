# Search Patients with Cerbo

Finds patients in Cerbo by search criteria.

## Endpoint

- **Method:** `GET`
- **Path:** `/patients/search`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Search Patients](https://docs.cer.bo/#tag/Patients/operation/searchPatients)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `last_name` | query | `string` | no | Match patients with given last name. Allows wildcard: smith% will match “Smith”,”Smithson”,”Simthe” etc) |
| `first_name` | query | `string` | no | Match patients with given first name Allows wildcard: ben% will match “Ben”,”Benjamin”,”Bennett” etc) |
| `email` | query | `string` | no | Match patients with given email as their primary or secondary address Allows wildcard: %@gmail.com will match all patients with Gmail addresses |
| `username` | query | `string` | no | Match patients with given patient portal username |
| `dob` | query | `string` | no | Match patients with given date of birth (preferred format is yyyy-mmdd). No wildcards allowed |
| `timezone` | query | `string` | no | Match patients with given timezone (Must be a canonical timezone https://en.wikipedia.org/wiki/List_of_tz_database_time_zones). |
