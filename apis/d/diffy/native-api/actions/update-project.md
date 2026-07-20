# Update Project with Diffy

Updates an existing project in Diffy.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:id`
- **Base URL:** `https://app.diffy.website/api`
- **Official documentation:** [Update Project](https://app.diffy.website/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Project ID. |
| `name` | body | `string` | no | Project name. |
| `production` | body | `string` | yes | Production environment URL. |
| `urls[]` | body | `array<string>` | yes | Project URLs to track |
| `breakpoints[]` | body | `array<number>` | yes | Viewport widths to capture |
