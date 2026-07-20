# Update Tag Status with Weekdone

Updates status text for a tag in Weekdone.

## Endpoint

- **Method:** `PATCH`
- **Path:** `tag/:tagId/status`
- **Base URL:** `https://api.weekdone.com/1/`
- **Official documentation:** [Update Tag Status](https://weekdone.com/developer#h-tags)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `status` | body | `string` | yes |
| `tagId` | path | `number` | yes |
