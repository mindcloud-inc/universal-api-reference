# Update Order with retailCRM

Updates an existing order in retailCRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/orders/:externalId/edit`
- **Base URL:** `{accountUrl}/api/v5`

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `externalId` | path | `string` | yes | — |
| `by` | body | `list` | no | Accepted values: `externalId`, `id`. |
| `site` | body | `list` | yes | — |
| `order.managerComment` | body | `string` | no | — |
