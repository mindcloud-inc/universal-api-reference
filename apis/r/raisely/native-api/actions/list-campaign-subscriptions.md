# List Campaign Subscriptions with Raisely

Retrieves subscriptions from a Raisely campaign.

## Endpoint

- **Method:** `GET`
- **Path:** `/campaigns/:campaign/subscriptions`
- **Base URL:** `https://api.raisely.com/v3`
- **Official documentation:** [List Campaign Subscriptions](https://developers.raisely.com/reference/getcampaignssubscriptions)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign` | path | `string` | yes | The `uuid`, `path` or domain of the campaign to associate with the request |
| `private` | query | `boolean` | no | Returns the full record when authenticated |
| `q` | query | `string` | no | Search query to find records matching |
| `mode` | query | `string` | no | Filter Subscription based on their mode value |
| `status` | query | `string` | no | Filter Subscription based on their status value |
| `source` | query | `string` | no | Filter subscriptions based on their source value of "OFFLINE" or "ONLINE" |
| `userUuid` | query | `string` | no | Filter Subscription based on their userUuid value |
| `organisation` | query | `string` | no | Filter by organisation uuid |
| `profile` | query | `string` | no | Filter by profile path or uuid |
| `user` | query | `string` | no | Filter by user uuid |
