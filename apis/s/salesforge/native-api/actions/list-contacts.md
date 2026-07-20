# List Contacts with Salesforge

Retrieves contacts from Salesforge.

## Endpoint

- **Method:** `GET`
- **Path:** `/public/v2/workspaces/:workspaceID/contacts`
- **Base URL:** `https://api.salesforge.ai`
- **Official documentation:** [List Contacts](https://api.salesforge.ai/public/v2/docs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceID` | path | `string` | yes |
| `tag_ids[]` | query | `array<string>` | no |
| `not_in_sequence_id` | query | `string` | no |
| `validation_statuses[]` | query | `array<string>` | no |
