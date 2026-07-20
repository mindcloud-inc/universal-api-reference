# Add Tags with Hy.page

## Endpoint

- **Method:** `POST`
- **Path:** `/hyax-api/v1/people/tags/add`
- **Base URL:** `https://platform.hyax.com`
- **Official documentation:** [Add Tags](https://platform.hyax.com/api-docs/people-tags-add)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Person email address. |
| `tags[]` | body | `array<string>` | yes | Tags to add. |
