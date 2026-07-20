# Publish Record with DatoCMS

## Endpoint

- **Method:** `PUT`
- **Path:** `/items/:itemId/publish`
- **Base URL:** `https://site-api.datocms.com`
- **Official documentation:** [Publish Record](https://www.datocms.com/docs/content-management-api/resources/item/publish)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `itemId` | path | `string` | yes | — |
| `content_in_locales` | body | `list<string>` | no | Locales to publish in selective publish mode. |
| `non_localized_content` | body | `boolean` | no | Whether to include non-localized content in selective publish mode. |
| `recursive` | query | `boolean` | no | Publish parent records recursively when required by tree relationships. |
