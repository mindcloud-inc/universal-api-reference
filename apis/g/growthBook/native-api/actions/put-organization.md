# Edit a single organization (only for super admins on multi-org Enterprise Plan only) with GrowthBook

Updates an existing organization in GrowthBook.

## Endpoint

- **Method:** `PUT`
- **Path:** `/organizations/:id`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Edit a single organization (only for super admins on multi-org Enterprise Plan only)](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The id of the requested resource |
| `name` | body | `string` | no | The name of the organization |
| `externalId` | body | `string` | no | An optional identifier that you use within your company for the organization |
