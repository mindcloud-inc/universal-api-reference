# Get Campaign with Raisely

Retrieves a campaign from Raisely.

## Endpoint

- **Method:** `GET`
- **Path:** `/campaigns/:campaign`
- **Base URL:** `https://api.raisely.com/v3`
- **Official documentation:** [Get Campaign](https://developers.raisely.com/reference/getcampaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign` | path | `string` | yes | The `uuid`, `path` or domain of the campaign to associate with the request |
| `private` | query | `boolean` | no | Returns the full record when authenticated |
| `pruneConfig` | query | `boolean` | no | In private queries, removes the campaign.config to reduce request size |
| `includeTags` | query | `boolean` | no | Also include any tags on this record (if applicable) |
