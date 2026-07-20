# Update Doc with Dart

Updates an existing doc in Dart.

## Endpoint

- **Method:** `PUT`
- **Path:** `/docs/:id`
- **Base URL:** `https://app.dartai.com/api/v0/public`
- **Official documentation:** [Update Doc](https://app.dartai.com/api/v0/public/docs/#/Doc/updateDoc)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | no |
| `item.folder` | body | `string` | no |
| `item.id` | body | `string` | no |
| `item.text` | body | `string` | no |
| `item.title` | body | `string` | no |
