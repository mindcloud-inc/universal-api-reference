# List External Shares with pixx.io

Retrieves external shares from your pixx.io workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/externalShares`
- **Base URL:** `https://mindcloudpixx260413.px.media/api/v1`
- **Official documentation:** [List External Shares](https://api.pixxio.com/docs/openapi)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collectionIDs` | query | `number<number>` | no | Filter external shares by collection IDs. Send multiple values as a array. |
| `isActive` | query | `boolean` | no | Filter external shares by active status. |
| `name` | query | `string` | no | Filter external shares by name. |
