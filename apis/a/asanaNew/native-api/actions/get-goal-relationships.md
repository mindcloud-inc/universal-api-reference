# Get goal relationships with Asana

Retrieves goal relationships from Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `goal_relationships`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get goal relationships](https://developers.asana.com/reference/getgoalrelationships)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `opt_pretty` | query | `boolean` | no |
| `supported_goal` | query | `string` | yes |
| `resource_subtype` | query | `string` | no |
| `opt_fields` | query | `list<string>` | no |
