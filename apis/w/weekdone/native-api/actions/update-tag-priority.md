# Update Tag Priority with Weekdone

Updates priority status for a tag in Weekdone.

## Endpoint

- **Method:** `PATCH`
- **Path:** `tag/:tagId/priority`
- **Base URL:** `https://api.weekdone.com/1/`
- **Official documentation:** [Update Tag Priority](https://weekdone.com/developer#h-tags)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `priority` | body | `number` | yes |
| `tagId` | path | `number` | yes |
