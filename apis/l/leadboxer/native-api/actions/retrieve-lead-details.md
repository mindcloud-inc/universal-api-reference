# Retrieve Lead Details with Leadboxer

Retrieves lead details from Leadboxer.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/leads/{{leadId}}`
- **Base URL:** `https://data.leadboxer.com`
- **Official documentation:** [Retrieve Lead Details](https://developers.leadboxer.com/reference/leaddetail)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `leadId` | path | `string` | yes |
| `email` | query | `string` | yes |
| `site` | query | `string` | yes |
