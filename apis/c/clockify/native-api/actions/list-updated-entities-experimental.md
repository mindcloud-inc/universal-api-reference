# List Updated Entities (Experimental) with Clockify

Lists experimentally tracked updated entities in Clockify.

## Endpoint

- **Method:** `GET`
- **Path:** `workspaces/:workspaceId/entities/updated`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [List Updated Entities (Experimental)](https://docs.developer.clockify.me/#tag/Entity-changes-(Experimental)/operation/getUpdatedEntityInfo)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `type[]` | query | `array<string>` | yes |
| `end` | query | `string` | no |
| `start` | query | `string` | no |
