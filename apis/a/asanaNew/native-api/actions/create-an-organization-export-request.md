# Create an organization export request with Asana

Creates an organization export request in Asana.

## Endpoint

- **Method:** `POST`
- **Path:** `organization_exports`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Create an organization export request](https://developers.asana.com/reference/createorganizationexport)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `data.organization` | body | `string` | yes |
| `opt_pretty` | query | `boolean` | no |
| `opt_fields` | query | `list<string>` | no |
