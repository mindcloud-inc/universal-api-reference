# Get a workspace's custom fields with Asana

Retrieves a workspace's custom fields from Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `workspaces/:workspace_gid/custom_fields`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get a workspace's custom fields](https://developers.asana.com/reference/getcustomfieldsforworkspace)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `opt_fields[]` | query | `array<string>` | no | — |
| `workspace_gid` | path | `string` | yes | Path parameter: workspace_gid |
