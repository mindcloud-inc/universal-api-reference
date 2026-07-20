# List Teams with Missive

Retrieves teams from your Missive workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/teams`
- **Base URL:** `https://public.missiveapp.com/v1`
- **Official documentation:** [List Teams](https://missiveapp.com/docs/developers/rest-api/endpoints#list-teams)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization` | query | `string` | no | Organization ID to filter teams. |
