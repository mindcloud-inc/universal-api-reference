# Get Customer with retailCRM

Retrieves a customer from retailCRM by external ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/customers/:externalId`
- **Base URL:** `{accountUrl}/api/v5`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `externalId` | path | `string` | yes | — |
| `by` | query | `list` | no | Accepted values: `externalId`, `id`. |
| `site` | query | `list` | yes | — |
