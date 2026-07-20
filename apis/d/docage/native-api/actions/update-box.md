# Update Box with Docage

Updates an existing box in Docage.

## Endpoint

- **Method:** `PUT`
- **Path:** `/Boxes/:id`
- **Base URL:** `https://api.docage.com`
- **Official documentation:** [Update Box](https://documentation.docage.com/modifier-un-classeur-23707565e0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Description` | body | `string` | no | An optional updated box description. |
| `id` | path | `string` | yes | The Docage box ID. |
| `Name` | body | `string` | no | The updated box name. |
