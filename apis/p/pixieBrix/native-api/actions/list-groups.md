# List Groups with PixieBrix

Retrieves groups in a PixieBrix organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/organizations/:organization_pk/groups/`
- **Base URL:** `https://app.pixiebrix.com`
- **Official documentation:** [List Groups](https://app.pixiebrix.com/api/docs/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_pk` | path | `string` | yes | PixieBrix organization identifier. |
