# List Templates with API Template

Retrieves templates from API Template.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/list-templates`
- **Base URL:** `https://rest.apitemplate.io`
- **Official documentation:** [List Templates](https://apitemplate.io/apiv2/#tag/Template-Management/operation/list-templates)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `format` | query | `string` | no | Filter templates by format. |
| `group_name` | query | `string` | no | Filter templates by group name. |
| `template_id` | query | `string` | no | Return only the matching template ID. |
| `with_layer_info` | query | `string` | no | Include layer information in the template response. |
