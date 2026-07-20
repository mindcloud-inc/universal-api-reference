# Create a New Collection with Histre

Creates a new collection in Histre.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/collections/`
- **Base URL:** `https://histre.com`
- **Official documentation:** [Create a New Collection](https://histre.com/features/api/collections/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Title of the collection to create. |
| `description` | body | `string` | no | Optional description of the collection. |
