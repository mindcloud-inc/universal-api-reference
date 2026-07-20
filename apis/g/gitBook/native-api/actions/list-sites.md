# List Sites with GitBook

Retrieves sites from a GitBook organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/orgs/:organizationId/sites`
- **Base URL:** `https://api.gitbook.com/v1`
- **Official documentation:** [List Sites](https://gitbook.com/docs/developers/gitbook-api/api-reference/docs-sites)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `string` | yes | — |
| `published` | query | `boolean` | no | — |
| `space` | query | `string` | no | — |
| `title` | query | `string` | no | — |
| `type[]` | query | `array<string>` | no | Send multiple values as a array. |
