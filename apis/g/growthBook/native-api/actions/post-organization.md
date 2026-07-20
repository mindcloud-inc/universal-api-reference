# Create a single organization (only for super admins on multi-org Enterprise Plan only) with GrowthBook

Creates a new organization in GrowthBook.

## Endpoint

- **Method:** `POST`
- **Path:** `/organizations`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Create a single organization (only for super admins on multi-org Enterprise Plan only)](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The name of the organization |
| `externalId` | body | `string` | no | An optional identifier that you use within your company for the organization |
