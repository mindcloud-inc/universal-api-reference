# List Campaigns with Raisely

Retrieves campaigns from Raisely.

## Endpoint

- **Method:** `GET`
- **Path:** `/campaigns`
- **Base URL:** `https://api.raisely.com/v3`
- **Official documentation:** [List Campaigns](https://developers.raisely.com/reference/getcampaigns)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `private` | query | `boolean` | no | Returns the full record when authenticated |
| `q` | query | `string` | no | Search query to find records matching |
| `path` | query | `string` | no | Filter Campaign based on their path value |
| `mode` | query | `string` | no | Filter Campaign based on their mode value |
| `status` | query | `string` | no | Filter Campaign based on their status value |
| `pruneConfig` | query | `boolean` | no | In private queries, removes the campaign.config to reduce request size |
| `includeTags` | query | `boolean` | no | Also include any tags on this collection (if applicable) |
