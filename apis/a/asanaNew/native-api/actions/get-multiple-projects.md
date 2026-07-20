# Get multiple projects with Asana

Retrieves projects from Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `projects`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get multiple projects](https://developers.asana.com/reference/getprojects)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `archived` | query | `boolean` | no |
| `limit` | query | `number` | no |
| `offset` | query | `string` | no |
| `opt_fields[]` | query | `array<string>` | no |
| `team` | query | `string` | no |
| `workspace` | query | `string` | no |
