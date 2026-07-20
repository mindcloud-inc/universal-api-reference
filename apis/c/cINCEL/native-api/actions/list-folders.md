# List Folders with CINCEL

## Endpoint

- **Method:** `GET`
- **Path:** `/teams/:team/folders`
- **Base URL:** `https://api.cincel.digital/v3`
- **Official documentation:** [List Folders](https://docs.cincel.digital/v3/digital-signature#get-/teams/-team-/folders)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team` | path | `string` | yes | UUID of the team whose folders should be listed. |
| `include_deleted` | query | `boolean` | no | Include deleted folders when true. |
| `name_like` | query | `string` | no | Filter folders by partial name match. |
