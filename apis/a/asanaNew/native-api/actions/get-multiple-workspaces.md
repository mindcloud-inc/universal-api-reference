# Get multiple workspaces with Asana

Retrieves workspaces from Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `workspaces`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get multiple workspaces](https://developers.asana.com/reference/getworkspaces)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `opt_pretty` | query | `boolean` | no | Comma-separated list of fields to include in each workspace record. |
| `opt_fields` | query | `list<string>` | no | — |
