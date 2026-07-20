# List Orders for Job with VSCO Workspace

Retrieves orders for a job in VSCO Workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/job/:jobId/order`
- **Base URL:** `https://workspace.vsco.co/api/v2`
- **Official documentation:** [List Orders for Job](https://workspace.vsco.co/api/#operation/listResourceJobOrders)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `jobId` | path | `string` | yes |
