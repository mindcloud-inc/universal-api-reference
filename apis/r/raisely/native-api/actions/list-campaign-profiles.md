# List Campaign Profiles with Raisely

Retrieves profiles from a Raisely campaign.

## Endpoint

- **Method:** `GET`
- **Path:** `/campaigns/:campaign/profiles`
- **Base URL:** `https://api.raisely.com/v3`
- **Official documentation:** [List Campaign Profiles](https://developers.raisely.com/reference/getcampaignsprofiles)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign` | path | `string` | yes | The `uuid`, `path` or domain of the campaign to associate with the request |
| `private` | query | `boolean` | no | Returns the full record when authenticated |
| `q` | query | `string` | no | Search query to find records matching |
