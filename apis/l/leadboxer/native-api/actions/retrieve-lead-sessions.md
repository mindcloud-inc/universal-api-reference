# Retrieve Lead Sessions with Leadboxer

Retrieves lead sessions in Leadboxer by lead ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/leads/sessions`
- **Base URL:** `https://data.leadboxer.com`
- **Official documentation:** [Retrieve Lead Sessions](https://developers.leadboxer.com/reference/getsessions)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `leadId` | query | `string` | yes |
| `limit` | query | `number` | yes |
| `site` | query | `string` | yes |
