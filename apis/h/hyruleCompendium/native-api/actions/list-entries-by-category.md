# List Entries by Category with Hyrule Compendium

## Endpoint

- **Method:** `GET`
- **Path:** `/compendium/category/:category`
- **Base URL:** `https://api.hyrule-compendium.com/v3`
- **Official documentation:** [List Entries by Category](https://gadhagod.github.io/Hyrule-Compendium-API/#/compendium-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category` | path | `list` | yes | Documented compendium category. Accepted values: `0`, `1`, `2`, `3`, `4`. |
| `game` | query | `list` | no | Supported game; defaults to Breath of the Wild. Accepted values: `0`, `1`. |
