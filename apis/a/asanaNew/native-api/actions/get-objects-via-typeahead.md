# Get objects via typeahead with Asana

Finds objects in Asana by typeahead.

## Endpoint

- **Method:** `GET`
- **Path:** `workspaces/:workspace_gid/typeahead`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get objects via typeahead](https://developers.asana.com/reference/typeaheadforworkspace)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace_gid` | path | `string` | yes |
| `resource_type` | query | `string` | yes |
| `type` | query | `string` | no |
| `query` | query | `string` | no |
| `count` | query | `number` | no |
| `opt_pretty` | query | `boolean` | no |
| `opt_fields` | query | `list<string>` | no |
