# Get Tag Type with Cinode

Retrieves a tag type from Cinode.

## Endpoint

- **Method:** `GET`
- **Path:** `/v0.2/companies/:companyId/tag-types/:id`
- **Base URL:** `https://api.cinode.com`
- **Official documentation:** [Get Tag Type](https://api.cinode.com/docs/index.html#/TagTypes/GetTagType)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `number` | yes | Cinode company identifier. |
| `id` | path | `number` | yes | Identifier of the tag type. |
