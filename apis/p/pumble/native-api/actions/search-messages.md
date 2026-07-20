# Search Messages with Pumble

Finds messages in Pumble by search criteria.

## Endpoint

- **Method:** `POST`
- **Path:** `/searchMessages`
- **Base URL:** `https://pumble-api-keys.addons.marketplace.cake.com`
- **Official documentation:** [Search Messages](https://pumble-api-keys.addons.marketplace.cake.com/api-docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from[]` | body | `array<string>` | no | Array of user identifiers or names to filter search results by sender. |
| `in[]` | body | `array<string>` | no | Array of channel or conversation identifiers to search within. |
| `text` | body | `string` | no | — |
