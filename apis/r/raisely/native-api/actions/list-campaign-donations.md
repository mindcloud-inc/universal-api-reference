# List Campaign Donations with Raisely

Retrieves donations from a Raisely campaign.

## Endpoint

- **Method:** `GET`
- **Path:** `/campaigns/:campaign/donations`
- **Base URL:** `https://api.raisely.com/v3`
- **Official documentation:** [List Campaign Donations](https://developers.raisely.com/reference/getcampaignsdonations)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign` | path | `string` | yes | The `uuid`, `path` or domain of the campaign to associate with the request |
| `private` | query | `boolean` | no | Returns the full record when authenticated |
| `q` | query | `string` | no | Search query to find records matching |
| `type` | query | `string` | no | Filter Donation based on their type value |
| `currency` | query | `string` | no | Filter Donation based on their currency value |
| `isSuspicious` | query | `boolean` | no | Filter Donation based on their isSuspicious value |
| `status` | query | `string` | no | Filter Donation based on their status value |
| `mode` | query | `string` | no | Filter Donation based on their mode value |
| `user` | query | `string` | no | Filter by user uuid |
| `organisation` | query | `string` | no | Filter by organisation uuid |
| `profile` | query | `string` | no | Filter by profile path or uuid |
| `subscription` | query | `string` | no | Filter by subscription uuid |
| `matchedDonationConfig` | query | `string` | no | Filter by matched donation config path or uuid |
