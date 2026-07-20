# Remove Tags with Hy.page

## Endpoint

- **Method:** `POST`
- **Path:** `/hyax-api/v1/people/tags/remove`
- **Base URL:** `https://platform.hyax.com`
- **Official documentation:** [Remove Tags](https://platform.hyax.com/api-docs/people-tags-remove)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Person email address. |
| `tags[]` | body | `array<string>` | yes | Tags to remove. |
