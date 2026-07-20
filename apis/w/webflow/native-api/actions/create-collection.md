# Create Collection with Webflow

Creates a new collection in Webflow.

## Endpoint

- **Method:** `POST`
- **Path:** `/sites/:site_id/collections`
- **Base URL:** `https://api.webflow.com/v2`
- **Official documentation:** [Create Collection](https://developers.webflow.com/data/reference/cms/collections/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `site_id` | path | `string` | yes | The unique identifier of the site. |
| `displayName` | body | `string` | yes | Display name for the collection. |
| `singularName` | body | `string` | yes | Singular noun for the collection. |
| `slug` | body | `string` | yes | Slug for the collection. |
| `fields` | body | `list<object>` | no | List of collection field definitions. |
