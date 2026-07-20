# List Contacts with respond.io

Retrieves contacts from respond.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/contact/list`
- **Base URL:** `https://api.respond.io/v2`
- **Official documentation:** [List Contacts](https://stoplight.io/api/v1/projects/respond/api/nodes/v2/contact-api.yml/paths/~1contact~1list/post?fromExportButton=true&snapshotType=http_operation)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | body | `string` | no | Search criteria payload. |
| `timezone` | body | `string` | no | Timezone used for filter evaluation. |
