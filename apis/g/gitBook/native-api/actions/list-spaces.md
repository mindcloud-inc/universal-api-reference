# List Spaces with GitBook

Retrieves spaces from a GitBook organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/orgs/:organizationId/spaces`
- **Base URL:** `https://api.gitbook.com/v1`
- **Official documentation:** [List Spaces](https://gitbook.com/docs/developers/gitbook-api/api-reference/spaces)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `organizationId` | path | `string` | yes |
