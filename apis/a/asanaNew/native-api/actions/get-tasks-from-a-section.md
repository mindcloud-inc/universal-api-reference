# Get tasks from a section with Asana

Retrieves tasks from a section in Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `sections/:section_gid/tasks`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get tasks from a section](https://developers.asana.com/reference/gettasksforsection)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `section_gid` | path | `string` | yes |
| `opt_pretty` | query | `boolean` | no |
| `completed_since` | query | `string` | no |
| `opt_fields` | query | `list<string>` | no |
