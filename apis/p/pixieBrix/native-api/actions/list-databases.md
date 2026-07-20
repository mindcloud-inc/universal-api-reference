# List Databases with PixieBrix

Retrieves databases from a PixieBrix organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/organizations/:organization_pk/databases/`
- **Base URL:** `https://app.pixiebrix.com`
- **Official documentation:** [List Databases](https://docs.pixiebrix.com/developer-api/database-apis)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_pk` | path | `string` | yes | PixieBrix organization identifier. |
| `q` | query | `string` | no | Search text for narrowing database results. |
