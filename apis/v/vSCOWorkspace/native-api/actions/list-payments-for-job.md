# List Payments for Job with VSCO Workspace

Retrieves payments for a job in VSCO Workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/job/:id/payment`
- **Base URL:** `https://workspace.vsco.co/api/v2`
- **Official documentation:** [List Payments for Job](https://workspace.vsco.co/api/#operation/listResourceJobPayment)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
