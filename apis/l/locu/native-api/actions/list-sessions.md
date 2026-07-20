# List Sessions with Locu

Retrieves a paginated list of sessions from Locu.

## Endpoint

- **Method:** `GET`
- **Path:** `/sessions`
- **Base URL:** `https://api.locu.app/api/v1`
- **Official documentation:** [List Sessions](https://locu.app/api/docs#tag/sessions)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `orderBy` | query | `string` | no |
| `order` | query | `string` | no |
| `startAfter` | query | `string` | no |
| `startBefore` | query | `string` | no |
| `includeActivities` | query | `boolean` | no |
