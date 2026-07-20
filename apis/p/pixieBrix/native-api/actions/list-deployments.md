# List Deployments with PixieBrix

Retrieves deployments from a PixieBrix organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/organizations/:organization_pk/deployments/`
- **Base URL:** `https://app.pixiebrix.com`
- **Official documentation:** [List Deployments](https://docs.pixiebrix.com/developer-api/deployment-apis)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_pk` | path | `string` | yes | PixieBrix organization identifier. |
