# List Organization Members with GitBook

Retrieves members from a GitBook organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/orgs/:organizationId/members`
- **Base URL:** `https://api.gitbook.com/v1`
- **Official documentation:** [List Organization Members](https://gitbook.com/docs/developers/gitbook-api/api-reference/organizations)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `organizationId` | path | `string` | yes |
| `role` | query | `string` | no |
| `search` | query | `string` | no |
| `sort` | query | `string` | no |
