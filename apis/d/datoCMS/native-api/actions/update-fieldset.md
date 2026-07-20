# Update Fieldset with DatoCMS

## Endpoint

- **Method:** `PUT`
- **Path:** `/fieldsets/:fieldsetId`
- **Base URL:** `https://site-api.datocms.com`
- **Official documentation:** [Update Fieldset](https://www.datocms.com/docs/content-management-api/resources/fieldset/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fieldsetId` | path | `string` | yes | Fieldset ID. |
| `data.attributes` | body | `object` | yes | Fieldset attributes payload. |
| `data.attributes.title` | body | `string` | no | — |
| `data.attributes.hint` | body | `string` | no | — |
| `data.attributes.position` | body | `number` | no | — |
| `data.attributes.collapsible` | body | `boolean` | no | — |
| `data.attributes.start_collapsed` | body | `boolean` | no | — |
