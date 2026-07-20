# Get Organization Shorten Counts By Group with Bitly

Retrieves organization shorten counts by group in Bitly.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organization_guid/shorten_counts_by_group`
- **Base URL:** `https://api-ssl.bitly.com/v4`
- **Official documentation:** [Get Organization Shorten Counts By Group](https://dev.bitly.com/api-reference#getOrganizationShortenCountsByGroup)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `organization_guid` | path | `string` | yes |
| `unit` | query | `string` | yes |
| `unit_reference` | query | `string` | no |
| `units` | query | `number` | yes |
