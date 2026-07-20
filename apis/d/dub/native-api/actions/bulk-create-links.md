# Bulk Create Links with Dub

Creates links in Dub in bulk.

## Endpoint

- **Method:** `POST`
- **Path:** `/links/bulk`
- **Base URL:** `https://api.dub.co`
- **Official documentation:** [Bulk Create Links](https://dub.co/docs/api-reference/links/bulk-create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `links[]` | body | `array<object>` | yes | JSON array of link objects. Each item must include `url`. Common optional keys include `domain`, `key`, `title`, `externalId`, `tagIds`, `tagNames`, `folderId`, `comments`, and `expiresAt`. |
| `links[].url` | body | `string` | no | Destination URL for this link row. Required by Dub for each link object. |
| `links[].domain` | body | `string` | no | Short-link domain for this row. |
| `links[].key` | body | `string` | no | Custom short-link slug for this row. |
| `links[].title` | body | `string` | no | Optional title for this row. |
| `links[].externalId` | body | `string` | no | External identifier for this row. |
| `links[].tagIds[]` | body | `array<string>` | no | Tag IDs assigned to this row. |
| `links[].tagNames[]` | body | `array<string>` | no | Tag names assigned to this row. |
| `links[].folderId` | body | `string` | no | Folder ID assigned to this row. |
| `links[].comments` | body | `string` | no | Comments for this row. |
| `links[].expiresAt` | body | `date` | no | ISO-8601 expiration timestamp for this row. |
