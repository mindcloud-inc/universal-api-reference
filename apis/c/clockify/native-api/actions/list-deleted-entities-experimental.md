# List Deleted Entities (Experimental) with Clockify

Lists experimentally tracked deleted entities in Clockify.

## Endpoint

- **Method:** `GET`
- **Path:** `workspaces/:workspaceId/entities/deleted`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [List Deleted Entities (Experimental)](https://docs.developer.clockify.me/#tag/Entity-changes-(Experimental)/operation/getDeletedEntityInfo)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `type[]` | query | `array<string>` | yes |
| `end` | query | `string` | no |
| `start` | query | `string` | no |
