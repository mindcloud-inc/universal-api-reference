# List Missing Update Version Endpoints with Action1

Retrieves endpoints missing a specific update version in Action1.

## Endpoint

- **Method:** `GET`
- **Path:** `/updates/:orgId/:packageId/versions/:versionId/endpoints`
- **Base URL:** `https://app.action1.com/api/3.0`
- **Official documentation:** [List Missing Update Version Endpoints](https://app.action1.com/apidocs/#/Software%20Deployment.%20Updates%20(Patches)/updates_orgId_packageId_versions_versionId_endpoints_get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orgId` | path | `string` | yes | Action1 organization ID. |
| `packageId` | path | `string` | yes | Missing update package ID. |
| `versionId` | path | `string` | yes | Update version ID. |
