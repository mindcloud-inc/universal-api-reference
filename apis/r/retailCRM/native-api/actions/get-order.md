# Get Order with retailCRM

Retrieves an order from retailCRM by external ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/orders/:externalId`
- **Base URL:** `{accountUrl}/api/v5`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `externalId` | path | `string` | yes | — |
| `by` | query | `list` | no | Accepted values: `externalId`, `id`. |
| `site` | query | `list` | yes | — |
