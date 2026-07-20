# List Project Webhooks with Zeplin

Retrieves a list of project webhooks from Zeplin.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{project_id}/webhooks`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [List Project Webhooks](https://docs.zeplin.dev/reference/getprojectwebhooks)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Project id |
| `status` | query | `string` | no | Filter by webhook status |
| `url_health` | query | `string` | no | Filter by health of webhook's URL |
