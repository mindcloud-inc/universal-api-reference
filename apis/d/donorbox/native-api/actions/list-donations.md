# List Donations with Donorbox

Retrieves donations from Donorbox.

## Endpoint

- **Method:** `GET`
- **Path:** `/donations`
- **Base URL:** `https://donorbox.org/api/v1`
- **Official documentation:** [List Donations](https://github.com/donorbox/donorbox-api#donations)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | no | — |
| `email` | query | `list<string>` | no | — |
| `date_from` | query | `string` | no | — |
| `date_to` | query | `string` | no | — |
| `campaign_id` | query | `list<string>` | no | — |
| `campaign_name` | query | `string` | no | — |
| `donor_id` | query | `string` | no | — |
| `first_name` | query | `string` | no | — |
| `last_name` | query | `string` | no | — |
| `amount[usd][min]` | query | `string` | no | Minimum USD amount filter. |
| `amount[usd][max]` | query | `string` | no | Maximum USD amount filter. |
