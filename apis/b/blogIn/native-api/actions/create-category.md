# Create Category with BlogIn

Creates a new category in BlogIn.

## Endpoint

- **Method:** `POST`
- **Path:** `/categories`
- **Base URL:** `https://blogin.co/api/rest`
- **Official documentation:** [Create Category](https://blogin.co/api/rest/docs/#create-new-category)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The name of the category. |
| `position` | body | `number` | no | The position of the category. |
| `locked` | body | `boolean` | no | Whether the category is locked. |
