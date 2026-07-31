# Get Entry with Hyrule Compendium

## Endpoint

- **Method:** `GET`
- **Path:** `/compendium/entry/:entry`
- **Base URL:** `https://api.hyrule-compendium.com/v3`
- **Official documentation:** [Get Entry](https://gadhagod.github.io/Hyrule-Compendium-API/#/compendium-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entry` | path | `string` | yes | Entry ID or name; names use underscores or URL encoding for spaces. |
| `game` | query | `list` | no | Supported game; defaults to Breath of the Wild. Accepted values: `0`, `1`. |
