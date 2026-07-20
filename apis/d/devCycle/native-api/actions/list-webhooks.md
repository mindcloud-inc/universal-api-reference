# List Webhooks with DevCycle

Retrieves webhooks from DevCycle.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/:project/webhooks`
- **Base URL:** `https://api.devcycle.com`
- **Official documentation:** [List Webhooks](https://docs.devcycle.com/management-api/#tag/Webhooks/operation/WebhooksController_findAll)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | path | `string` | no | Project key. |
