# List Contact Channels with respond.io

Retrieves contact channels from respond.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/contact/:identifier/channels`
- **Base URL:** `https://api.respond.io/v2`
- **Official documentation:** [List Contact Channels](https://stoplight.io/api/v1/projects/respond/api/nodes/v2/contact-api.yml/paths/~1contact~1%7Bidentifier%7D~1channels/get?fromExportButton=true&snapshotType=http_operation)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | Contact identifier (id:, email:, or phone:). |
