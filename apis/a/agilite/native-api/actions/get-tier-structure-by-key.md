# Get Tier Structure By Key with Agilite

Retrieves tier structure profiles from Agilite by tier keys.

## Endpoint

- **Method:** `GET`
- **Path:** `/tierstructures/getTierByKey`
- **Base URL:** `https://api.agilite.io`
- **Official documentation:** [Get Tier Structure By Key](https://docs.agilite.io/reference/gettierbykey)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include-meta-data` | query | `boolean` | no | Whether to include tier metadata. |
| `include-tier-entries` | query | `boolean` | no | Whether to include tier entries. |
| `include-values` | query | `boolean` | no | Whether to include tier values. |
| `tier-keys` | query | `string` | yes | Comma-separated tier structure keys to retrieve. |
| `values-output-format` | query | `list` | no | Value output format. |
