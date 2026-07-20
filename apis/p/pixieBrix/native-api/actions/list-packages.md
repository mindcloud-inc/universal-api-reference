# List Packages with PixieBrix

Retrieves packages from a PixieBrix organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/organizations/:organization_pk/bricks/`
- **Base URL:** `https://app.pixiebrix.com`
- **Official documentation:** [List Packages](https://docs.pixiebrix.com/developer-api/package-management-apis)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_pk` | path | `string` | yes | PixieBrix organization identifier. |
| `q` | query | `string` | no | Search text for narrowing package results. |
