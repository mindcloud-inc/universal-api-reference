# Retrieve Lead Events with Leadboxer

Retrieves lead events in Leadboxer by session ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/leads/events`
- **Base URL:** `https://data.leadboxer.com`
- **Official documentation:** [Retrieve Lead Events](https://developers.leadboxer.com/reference/getevents)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `sessionId` | query | `string` | yes |
| `limit` | query | `number` | yes |
| `site` | query | `string` | yes |
