# List Missing Updates with Action1

Retrieves missing updates from Action1 for an organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/updates/:orgId`
- **Base URL:** `https://app.action1.com/api/3.0`
- **Official documentation:** [List Missing Updates](https://app.action1.com/apidocs/#/Software%20Deployment.%20Updates%20(Patches)/updates_orgId_get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orgId` | path | `string` | yes | Provide an organization ID. |
