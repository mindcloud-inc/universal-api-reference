# List Organization Member Projects with Zeplin

Retrieves a list of organization member projects from Zeplin.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/{organization_id}/members/{member_id}/projects`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [List Organization Member Projects](https://docs.zeplin.dev/reference/getorganizationmemberprojects)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id` | path | `string` | yes | Organization id |
| `member_id` | path | `string` | yes | Member id |
