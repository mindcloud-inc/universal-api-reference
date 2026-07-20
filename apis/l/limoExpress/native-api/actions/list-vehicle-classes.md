# List Vehicle Classes with LimoExpress

Retrieves vehicle classes from the LimoExpress organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/integration/vehicle-classes`
- **Base URL:** `https://api.limoexpress.me`
- **Official documentation:** [List Vehicle Classes](https://api.limoexpress.me/api/docs/v1#/Vehicle%20Classes/getAllOrganisationVehicleClasses)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search_string` | query | `string` | no | Search across vehicle class fields. |
| `page` | query | `number` | no | Page number, default is 1. |
| `per_page` | query | `number` | no | Items per page, default is 20. |
