# List Members with Ghost

Retrieves members from Ghost.

## Endpoint

- **Method:** `GET`
- **Path:** `/members/`
- **Base URL:** `{adminDomain}/ghost/api/admin`
- **Official documentation:** [List Members](https://docs.ghost.org/admin-api/members/overview)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include` | query | `string` | no | Comma-separated related resources to include, such as labels or newsletters. |
