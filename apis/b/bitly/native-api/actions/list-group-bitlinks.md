# List Group Bitlinks with Bitly

Retrieves bitlinks for a group in Bitly.

## Endpoint

- **Method:** `GET`
- **Path:** `/groups/:group_guid/bitlinks`
- **Base URL:** `https://api-ssl.bitly.com/v4`
- **Official documentation:** [List Group Bitlinks](https://dev.bitly.com/api-reference#getBitlinksByGroup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `archived` | query | `string` | no | Filter archived bitlinks. |
| `campaign_guid` | query | `string` | no | Filter results to one campaign GUID. |
| `channel_guid` | query | `string` | no | Filter results to one channel GUID. |
| `created_after` | query | `string` | no | Filter to bitlinks created after this epoch timestamp. |
| `created_before` | query | `string` | no | Filter to bitlinks created before this epoch timestamp. |
| `custom_bitlink` | query | `string` | no | Filter custom bitlinks. |
| `deeplinks` | query | `string` | no | Filter bitlinks by deeplink status. |
| `domain_deeplinks` | query | `string` | no | Filter bitlinks by domain deeplink status. |
| `encoding_login[]` | query | `array<string>` | no | Filter results by encoding login values. |
| `group_guid` | path | `string` | yes | The Bitly group GUID. |
| `has_qr_codes` | query | `string` | no | Filter bitlinks by QR code presence. |
| `hostname_path_query` | query | `string` | no | Filter by hostname, path, or query text. |
| `launchpad_ids[]` | query | `array<string>` | no | Filter results by launchpad IDs. |
| `query` | query | `string` | no | Search bitlinks by query text. |
| `search_after` | query | `string` | no | Token used to request the next batch of results. |
| `size` | query | `number` | no | The number of bitlinks to return. |
| `tags[]` | query | `array<string>` | no | Filter results by tags. |
