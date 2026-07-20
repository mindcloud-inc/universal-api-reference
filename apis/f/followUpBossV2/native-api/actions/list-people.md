# List People with Follow Up Boss

Retrieves people from Follow Up Boss.

## Endpoint

- **Method:** `GET`
- **Path:** `people`
- **Base URL:** `https://api.followupboss.com/v1/`
- **Official documentation:** [List People](https://docs.followupboss.com/reference/people-get)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | query | `string` | no |
| `name` | query | `string` | no |
| `firstName` | query | `string` | no |
| `lastName` | query | `string` | no |
| `email` | query | `string` | no |
| `phone` | query | `string` | no |
| `stage` | query | `string` | no |
| `source` | query | `string` | no |
| `assignedTo` | query | `string` | no |
| `assignedUserId` | query | `number` | no |
| `assignedPondId` | query | `number` | no |
| `assignedLenderName` | query | `string` | no |
| `assignedLenderId` | query | `number` | no |
| `contacted` | query | `boolean` | no |
| `priceAbove` | query | `number` | no |
| `priceBelow` | query | `number` | no |
| `smartListId` | query | `number` | no |
| `tags` | query | `string` | no |
| `lastActivityAfter` | query | `string` | no |
| `lastActivityBefore` | query | `string` | no |
| `sort` | query | `string` | no |
| `fields` | query | `string` | no |
| `includeTrash` | query | `boolean` | no |
| `includeUnclaimed` | query | `boolean` | no |
