# List Donations with Raisely

Retrieves donations from Raisely.

## Endpoint

- **Method:** `GET`
- **Path:** `/donations`
- **Base URL:** `https://api.raisely.com/v3`
- **Official documentation:** [List Donations](https://developers.raisely.com/reference/getdonations)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `private` | query | `boolean` | no | Returns the full record when authenticated |
| `q` | query | `string` | no | Search query to find records matching |
| `type` | query | `string` | no | Filter Donation based on their type value |
| `currency` | query | `string` | no | Filter Donation based on their currency value |
| `isSuspicious` | query | `boolean` | no | Filter Donation based on their isSuspicious value |
| `status` | query | `string` | no | Filter Donation based on their status value |
| `mode` | query | `string` | no | Filter Donation based on their mode value |
| `user` | query | `string` | no | Filter by user uuid |
| `campaign` | query | `string` | no | Filter by campaign path or uuid |
| `organisation` | query | `string` | no | Filter by organisation uuid |
| `profile` | query | `string` | no | Filter by profile path or uuid |
| `subscription` | query | `string` | no | Filter by subscription uuid |
| `matchedDonationConfig` | query | `string` | no | Filter by matched donation config path or uuid |
