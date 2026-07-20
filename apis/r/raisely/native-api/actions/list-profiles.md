# List Profiles with Raisely

Retrieves profiles from Raisely.

## Endpoint

- **Method:** `GET`
- **Path:** `/profiles`
- **Base URL:** `https://api.raisely.com/v3`
- **Official documentation:** [List Profiles](https://developers.raisely.com/reference/getprofiles)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign` | query | `string` | yes | The `uuid`, `path` or domain of the campaign to associate with the request |
| `private` | query | `boolean` | no | Returns the full record when authenticated |
| `q` | query | `string` | no | Search query to find records matching |
| `rank` | query | `string` | no | Rank profiles by total raised |
| `rankDonors` | query | `string` | no | Rank profiles by unique donors |
| `rankActivityTotal` | query | `string` | no | Rank profiles by activity total |
| `rankActivityTime` | query | `string` | no | Rank profiles by activity time |
