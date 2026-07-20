# List Organization Articles with Dev.to

Lists articles for a Dev.to organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:username/articles`
- **Base URL:** `https://dev.to/api`
- **Official documentation:** [List Organization Articles](https://developers.forem.com/api/v1#tag/organizations/operation/getOrgArticles)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `username` | path | `string` | yes | Organization username. |
