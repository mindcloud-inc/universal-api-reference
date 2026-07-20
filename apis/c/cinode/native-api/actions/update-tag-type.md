# Update Tag Type with Cinode

Updates an existing tag type in Cinode.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v0.2/companies/:companyId/tag-types/:id`
- **Base URL:** `https://api.cinode.com`
- **Official documentation:** [Update Tag Type](https://api.cinode.com/docs/index.html#/TagTypes/EditTagType)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `number` | yes | Cinode company identifier. |
| `id` | path | `number` | yes | Identifier of the tag type. |
| `name` | body | `string` | yes | Updated name of the tag type. |
