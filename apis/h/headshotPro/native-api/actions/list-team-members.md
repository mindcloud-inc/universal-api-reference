# List Team Members with HeadshotPro

Retrieves team members from HeadshotPro.

## Endpoint

- **Method:** `GET`
- **Path:** `/organization/team`
- **Base URL:** `https://server.headshotpro.com/api/v2`
- **Official documentation:** [List Team Members](https://www.headshotpro.com/api/team-members)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `string` | no | Optional member status filter: accepted, pending, or finished. |
