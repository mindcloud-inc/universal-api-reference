# List Flows with Celigo

## Endpoint

- **Method:** `GET`
- **Path:** `/flows`
- **Base URL:** `https://{apiHost}/v1`
- **Official documentation:** [List Flows](https://developer.celigo.com/api/api-reference/integrations-and-flows/flows)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `_integrationId` | query | `list<string>` | no | Only return flows in this integration. |
| `name` | query | `string` | no | Only return flows whose name contains this text (case-insensitive). |
| `disabled` | query | `boolean` | no | Only return disabled (true) or enabled (false) flows. |
| `sort_by` | query | `list<string>` | no | Sort by most recent execution; never-run flows come last. Accepted values: `lastExecutedAt`. |
| `order` | query | `list<string>` | no | Sort direction. Accepted values: `asc`, `desc`. |
| `externalId` | query | `string` | no | Only return flows with this exact external identifier. |
| `includeInstances` | query | `boolean` | no | Also return instance flows generated from multi-instance (abstract) flows. |
