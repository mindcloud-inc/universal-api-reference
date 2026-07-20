# Create Scheduled Publication with DatoCMS

## Endpoint

- **Method:** `POST`
- **Path:** `/items/:itemId/scheduled-publication`
- **Base URL:** `https://site-api.datocms.com`
- **Official documentation:** [Create Scheduled Publication](https://www.datocms.com/docs/content-management-api/resources/scheduled-publication/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `itemId` | path | `string` | yes | Record ID. |
| `data.attributes.publication_scheduled_at` | body | `date` | yes | ISO-8601 datetime for publication. |
