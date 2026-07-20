# List Users with Raisely

Retrieves users from Raisely.

## Endpoint

- **Method:** `GET`
- **Path:** `/users`
- **Base URL:** `https://api.raisely.com/v3`
- **Official documentation:** [List Users](https://developers.raisely.com/reference/getusers)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `private` | query | `boolean` | no | Returns the full record when authenticated |
| `q` | query | `string` | no | Search query to find records matching |
| `postcode` | query | `string` | no | Filter User based on their postcode value |
| `country` | query | `string` | no | Filter User based on their country value |
| `facebookId` | query | `string` | no | Filter User based on their facebookId value |
| `email` | query | `string` | no | Filter User based on their email value |
| `fullName` | query | `string` | no | Filter User based on their fullName value |
| `phone_number` | query | `string` | no | Filter User based on their phone_number value |
| `organisation` | query | `string` | no | Filter by organisation uuid |
