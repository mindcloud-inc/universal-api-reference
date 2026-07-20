# Create Fieldset with DatoCMS

## Endpoint

- **Method:** `POST`
- **Path:** `/item-types/:itemTypeId/fieldsets`
- **Base URL:** `https://site-api.datocms.com`
- **Official documentation:** [Create Fieldset](https://www.datocms.com/docs/content-management-api/resources/fieldset/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `itemTypeId` | path | `string` | yes | Model ID or API key. |
| `data.attributes.title` | body | `string` | yes | Fieldset title. |
