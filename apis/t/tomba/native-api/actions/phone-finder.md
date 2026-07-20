# Phone Finder with Tomba

Finds a phone number in Tomba.

## Endpoint

- **Method:** `GET`
- **Path:** `/phone-finder`
- **Base URL:** `https://api.tomba.io/v1`
- **Official documentation:** [Phone Finder](https://docs.tomba.io/api/phone#phone-finder)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `email` | query | `string` | yes |
| `domain` | query | `string` | no |
| `linkedin` | query | `string` | no |
| `full` | query | `boolean` | no |
