# Get multiple project templates with Asana

Retrieves project templates from Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `project_templates`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get multiple project templates](https://developers.asana.com/reference/getprojecttemplates)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `opt_pretty` | query | `boolean` | no | Asana opt pretty parameter. |
| `workspace` | query | `string` | no | Asana workspace parameter. |
| `team` | query | `string` | no | Asana team parameter. |
| `limit` | query | `number` | no | Asana limit parameter. |
| `offset` | query | `string` | no | Asana offset parameter. |
| `opt_fields` | query | `list<string>` | no | Asana opt fields parameter. |
