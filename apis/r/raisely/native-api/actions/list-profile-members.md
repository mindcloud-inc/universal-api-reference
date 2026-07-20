# List Profile Members with Raisely

Retrieves members from a Raisely profile.

## Endpoint

- **Method:** `GET`
- **Path:** `/profiles/:path/members`
- **Base URL:** `https://api.raisely.com/v3`
- **Official documentation:** [List Profile Members](https://developers.raisely.com/reference/getprofilesmembers)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `path` | path | `string` | yes | The `uuid` or `path` of the record |
| `campaign` | query | `string` | no | The `uuid`, `path` or domain of the campaign to associate with the request |
| `private` | query | `boolean` | no | Returns the full record when authenticated |
| `q` | query | `string` | no | Search query to find records matching |
