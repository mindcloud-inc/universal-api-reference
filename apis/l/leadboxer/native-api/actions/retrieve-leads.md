# Retrieve Leads with Leadboxer

Retrieves leads from Leadboxer.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/leads`
- **Base URL:** `https://data.leadboxer.com`
- **Official documentation:** [Retrieve Leads](https://developers.leadboxer.com/reference/users)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `site` | query | `string` | yes |
| `criteriaTimeFilter` | query | `string` | yes |
| `timeField` | query | `string` | yes |
| `limit` | query | `number` | no |
