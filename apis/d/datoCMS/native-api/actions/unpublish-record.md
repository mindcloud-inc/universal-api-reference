# Unpublish Record with DatoCMS

## Endpoint

- **Method:** `PUT`
- **Path:** `/items/:itemId/unpublish`
- **Base URL:** `https://site-api.datocms.com`
- **Official documentation:** [Unpublish Record](https://www.datocms.com/docs/content-management-api/resources/item/unpublish)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `itemId` | path | `string` | yes | — |
| `content_in_locales` | body | `list<string>` | no | Locales to unpublish selectively. |
