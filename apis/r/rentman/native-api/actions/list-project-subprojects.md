# List Project Subprojects with Rentman

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:id/subprojects`
- **Base URL:** `https://api.rentman.net`
- **Official documentation:** [List Project Subprojects](https://api.rentman.net/#operation/getProjectSubprojectCollection)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Numeric ID of the parent project. |
