# List Collections with GitBook

Retrieves collections from a GitBook organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/orgs/:organizationId/collections`
- **Base URL:** `https://api.gitbook.com/v1`
- **Official documentation:** [List Collections](https://gitbook.com/docs/developers/gitbook-api/api-reference/collections)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `nested` | query | `boolean` | no |
| `organizationId` | path | `string` | yes |
