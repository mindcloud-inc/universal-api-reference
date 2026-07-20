# Create a single project with GrowthBook

Creates a new project in GrowthBook.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Create a single project](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | — |
| `description` | body | `string` | no | — |
| `publicId` | body | `string` | no | URL-safe slug (lowercase letters, numbers, dashes). Auto-generated from name if not provided. |
| `settings` | body | `object` | no | Project settings. |
