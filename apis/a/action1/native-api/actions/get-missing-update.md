# Get Missing Update with Action1

Retrieves available update versions from Action1 for a package.

## Endpoint

- **Method:** `GET`
- **Path:** `/updates/:orgId/:packageId`
- **Base URL:** `https://app.action1.com/api/3.0`
- **Official documentation:** [Get Missing Update](https://app.action1.com/apidocs/#/Software%20Deployment.%20Updates%20(Patches)/updates_orgId_packageId_get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orgId` | path | `string` | yes | Action1 organization ID. |
| `packageId` | path | `string` | yes | Missing update package ID. |
