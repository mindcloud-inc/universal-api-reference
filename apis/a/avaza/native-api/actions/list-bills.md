# List Bills with Avaza

Retrieves bills from Avaza.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/Bill`
- **Base URL:** `https://api.avaza.com`
- **Official documentation:** [List Bills](https://api.avaza.com/#!/Bill/Bill_Get)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `UpdatedAfter` | query | `date` | no |
| `CompanyIDFK` | query | `number` | no |
