# Update Collection Details with Histre

Updates collection details in Histre.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/collections/[:book_id]/`
- **Base URL:** `https://histre.com`
- **Official documentation:** [Update Collection Details](https://histre.com/features/api/collections/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `book_id` | path | `string` | yes | Identifier of the Histre collection to update. |
| `title` | body | `string` | no | Optional new title for the collection. |
| `description` | body | `string` | no | Optional new description for the collection. |
