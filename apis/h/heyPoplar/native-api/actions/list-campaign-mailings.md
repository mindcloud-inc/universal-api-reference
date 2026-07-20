# List Campaign Mailings with HeyPoplar

Retrieves mailings for a HeyPoplar campaign.

## Endpoint

- **Method:** `GET`
- **Path:** `/campaign/:id/mailings`
- **Base URL:** `https://api.heypoplar.com/v1`
- **Official documentation:** [List Campaign Mailings](https://docs.heypoplar.com/api/endpoints/other-endpoints#fetch-campaign-mailings)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | ID of the campaign whose mailings should be returned. |
| `start_date` | query | `string` | no | Return only mailings created after this ISO8601 timestamp. |
| `end_date` | query | `string` | no | Return only mailings created before this ISO8601 timestamp. |
