# Create Tag Type with Cinode

Creates a tag type in Cinode.

## Endpoint

- **Method:** `POST`
- **Path:** `/v0.2/companies/:companyId/tag-types`
- **Base URL:** `https://api.cinode.com`
- **Official documentation:** [Create Tag Type](https://api.cinode.com/docs/index.html#/TagTypes/CreateTagType)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `number` | yes | Cinode company identifier. |
| `name` | body | `string` | yes | Name of the tag type. |
