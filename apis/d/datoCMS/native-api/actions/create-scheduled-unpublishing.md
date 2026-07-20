# Create Scheduled Unpublishing with DatoCMS

## Endpoint

- **Method:** `POST`
- **Path:** `/items/:itemId/scheduled-unpublishing`
- **Base URL:** `https://site-api.datocms.com`
- **Official documentation:** [Create Scheduled Unpublishing](https://www.datocms.com/docs/content-management-api/resources/scheduled-unpublishing/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `itemId` | path | `string` | yes | Record ID. |
| `data.attributes.unpublishing_scheduled_at` | body | `date` | yes | ISO-8601 datetime for unpublishing. |
