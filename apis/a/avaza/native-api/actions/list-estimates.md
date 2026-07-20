# List Estimates with Avaza

Retrieves estimates from Avaza.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/Estimate`
- **Base URL:** `https://api.avaza.com`
- **Official documentation:** [List Estimates](https://api.avaza.com/#!/Estimate/Estimate_Get)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `UpdatedAfter` | query | `date` | no |
| `CompanyIDFK` | query | `number` | no |
