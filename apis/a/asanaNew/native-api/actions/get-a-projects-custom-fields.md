# Get a project's custom fields with Asana

Retrieves a project's custom fields from Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `projects/:project_gid/custom_field_settings`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get a project's custom fields](https://developers.asana.com/reference/getcustomfieldsettingsforproject)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `project_gid` | path | `string` | yes |
| `opt_pretty` | query | `boolean` | no |
| `opt_fields` | query | `list<string>` | no |
