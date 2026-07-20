# Bulk Update Group Bitlinks with Bitly

Updates tags or archives multiple group bitlinks in Bitly.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/groups/:group_guid/bitlinks`
- **Base URL:** `https://api-ssl.bitly.com/v4`
- **Official documentation:** [Bulk Update Group Bitlinks](https://dev.bitly.com/api-reference#updateBitlinksByGroup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `action` | body | `string` | yes | The bulk update operation to apply. |
| `add_tags[]` | body | `array<string>` | no | Tags to add to the selected links. |
| `archive` | body | `boolean` | no | Whether to archive the selected links. |
| `group_guid` | path | `string` | yes | The Bitly group GUID. |
| `links[]` | body | `array<string>` | no | The bitlink IDs to update in bulk. |
| `remove_tags[]` | body | `array<string>` | no | Tags to remove from the selected links. |
