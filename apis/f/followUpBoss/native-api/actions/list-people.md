# List People with Follow Up Boss - Legacy

Retrieves people from Follow Up Boss - Legacy.

## Endpoint

- **Method:** `GET`
- **Path:** `people`
- **Base URL:** `https://api.followupboss.com/v1/`
- **Official documentation:** [List People](https://docs.followupboss.com/reference/people-get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `assignedLenderId` | query | `int32` | no |
| `assignedLenderName` | query | `string` | no |
| `assignedPondId` | query | `int32` | no |
| `assignedTo` | query | `string` | no |
| `assignedUserId` | query | `int32` | no |
| `contacted` | query | `boolean` | no |
| `custom*` | query | `string` | no |
| `email` | query | `string` | no |
| `fields` | query | `string` | no |
| `firstName` | query | `string` | no |
| `id` | query | `string` | no |
| `includeTrash` | query | `boolean` | no |
| `includeUnclaimed` | query | `boolean` | no |
| `lastActivityAfter` | query | `string` | no |
| `lastActivityBefore` | query | `string` | no |
| `lastName` | query | `string` | no |
| `name` | query | `string` | no |
| `phone` | query | `string` | no |
| `priceAbove` | query | `int32` | no |
| `priceBelow` | query | `int32` | no |
| `smartListId` | query | `int32` | no |
| `sort` | query | `string` | no |
| `source` | query | `string` | no |
| `stage` | query | `string` | no |
| `tags` | query | `string` | no |
