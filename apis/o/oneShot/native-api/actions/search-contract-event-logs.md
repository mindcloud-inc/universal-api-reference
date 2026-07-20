# Search Contract Event Logs with 1Shot

Finds contract event logs in 1Shot API.

## Endpoint

- **Method:** `POST`
- **Path:** `/events/:contractEventId/search`
- **Base URL:** `https://api.1shotapi.com/v0`
- **Official documentation:** [Search Contract Event Logs](https://docs.1shotapi.com/api/openapi.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `contractEventId` | path | `string` | yes |
| `startBlock` | body | `number` | no |
| `endBlock` | body | `number` | no |
| `topics` | body | `list<string>` | no |
