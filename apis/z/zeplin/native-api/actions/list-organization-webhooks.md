# List Organization Webhooks with Zeplin

Retrieves a list of organization webhooks from Zeplin.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/{organization_id}/webhooks`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [List Organization Webhooks](https://docs.zeplin.dev/reference/getorganizationwebhooks)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id` | path | `string` | yes | Organization id |
| `status` | query | `string` | no | Filter by webhook status |
| `url_health` | query | `string` | no | Filter by health of webhook's URL |
