# Delete Tag Type with Cinode

Deletes an existing tag type from Cinode.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v0.2/companies/:companyId/tag-types/:id`
- **Base URL:** `https://api.cinode.com`
- **Official documentation:** [Delete Tag Type](https://api.cinode.com/docs/index.html#/TagTypes/DeleteTagType)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `number` | yes | Cinode company identifier. |
| `id` | path | `number` | yes | Identifier of the tag type. |
