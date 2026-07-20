# List Organization Memberships with PixieBrix

Retrieves memberships for an organization in PixieBrix.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/organizations/:organization_pk/memberships/`
- **Base URL:** `https://app.pixiebrix.com`
- **Official documentation:** [List Organization Memberships](https://app.pixiebrix.com/api/docs/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_pk` | path | `string` | yes | PixieBrix organization identifier. |
