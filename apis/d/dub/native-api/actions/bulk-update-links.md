# Bulk Update Links with Dub

Updates links in Dub in bulk.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/links/bulk`
- **Base URL:** `https://api.dub.co`
- **Official documentation:** [Bulk Update Links](https://dub.co/docs/api-reference/links/bulk-update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `linkIds[]` | body | `array<string>` | no | IDs of the links to update. Use this field or `External IDs` to choose the target links. |
| `data` | body | `object` | no | Fields in this section are applied to every selected link. |
| `externalIds[]` | body | `array<string>` | no | External IDs of the links to update. Use this field or `Target Link IDs` to choose the target links. |
| `data.url` | body | `string` | no | Updated destination URL applied to every selected link in this batch. |
| `data.title` | body | `string` | no | Updated title applied to every selected link in this batch. |
| `data.description` | body | `string` | no | Updated description applied to every selected link in this batch. |
| `data.archived` | body | `boolean` | no | Archive or unarchive every selected link. |
| `data.trackConversion` | body | `boolean` | no | Enable or disable conversion tracking for every selected link. |
| `data.tagIds[]` | body | `array<string>` | no | Tag IDs to assign to every selected link. |
| `data.tagNames[]` | body | `array<string>` | no | Tag names to assign to every selected link. |
| `data.folderId` | body | `string` | no | Folder ID to assign to every selected link. |
| `data.comments` | body | `string` | no | Comments applied to every selected link. |
| `data.expiresAt` | body | `date` | no | ISO-8601 expiration timestamp applied to every selected link. |
| `data.expiredUrl` | body | `string` | no | Destination URL to use after expiration for every selected link. |
| `data.publicStats` | body | `boolean` | no | Make stats public or private for every selected link. |
| `data.utm_source` | body | `string` | no | UTM source applied to every selected link. |
| `data.utm_medium` | body | `string` | no | UTM medium applied to every selected link. |
| `data.utm_campaign` | body | `string` | no | UTM campaign applied to every selected link. |
| `data.utm_term` | body | `string` | no | UTM term applied to every selected link. |
| `data.utm_content` | body | `string` | no | UTM content applied to every selected link. |
