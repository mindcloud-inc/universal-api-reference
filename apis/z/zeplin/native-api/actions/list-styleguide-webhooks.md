# List Styleguide Webhooks with Zeplin

Retrieves a list of styleguide webhooks from Zeplin.

## Endpoint

- **Method:** `GET`
- **Path:** `/styleguides/{styleguide_id}/webhooks`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [List Styleguide Webhooks](https://docs.zeplin.dev/reference/getstyleguidewebhooks)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `styleguide_id` | path | `string` | yes | Styleguide id |
| `status` | query | `string` | no | Filter by webhook status |
| `url_health` | query | `string` | no | Filter by health of webhook's URL |
