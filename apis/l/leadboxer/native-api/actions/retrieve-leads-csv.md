# Retrieve Leads CSV with Leadboxer

Retrieves leads as a CSV export from Leadboxer.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/leads/export`
- **Base URL:** `https://data.leadboxer.com`
- **Official documentation:** [Retrieve Leads CSV](https://developers.leadboxer.com/reference/userscsv)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `site` | query | `string` | yes |
| `timeField` | query | `string` | yes |
| `limit` | query | `number` | no |
