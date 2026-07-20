# List Message Templates with respond.io

Retrieves message templates from respond.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/space/channel/:id/template`
- **Base URL:** `https://api.respond.io/v2`
- **Official documentation:** [List Message Templates](https://stoplight.io/api/v1/projects/respond/api/nodes/v2/space-api.yml/paths/~1space~1channel~1%7Bid%7D~1template/get?fromExportButton=true&snapshotType=http_operation)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Channel ID. |
